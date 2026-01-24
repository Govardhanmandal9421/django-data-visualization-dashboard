# Deployment Guide

## Local Development Setup

### Prerequisites
- Python 3.8 or higher
- pip (Python package installer)

### Quick Start
1. Clone the repository
2. Run the setup script:
   - **Windows**: Double-click `setup.bat`
   - **Linux/macOS**: Run `chmod +x setup.sh && ./setup.sh`

### Manual Setup
```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# Windows: venv\Scripts\activate
# Linux/macOS: source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run migrations
python manage.py makemigrations
python manage.py migrate

# Start development server
python manage.py runserver
```

## Production Deployment

### Heroku Deployment

1. **Install Heroku CLI** and login:
```bash
heroku login
```

2. **Create Heroku app**:
```bash
heroku create your-app-name
```

3. **Add buildpacks**:
```bash
heroku buildpacks:set heroku/python
```

4. **Set environment variables**:
```bash
heroku config:set DJANGO_SECRET_KEY=your-secret-key-here
heroku config:set DJANGO_DEBUG=False
heroku config:set DJANGO_ALLOWED_HOSTS=your-app-name.herokuapp.com
```

5. **Deploy**:
```bash
git push heroku main
```

6. **Run migrations**:
```bash
heroku run python manage.py migrate
```

### AWS EC2 Deployment

1. **Launch EC2 instance** (Ubuntu 20.04 LTS recommended)

2. **SSH into instance**:
```bash
ssh -i your-key.pem ubuntu@your-instance-ip
```

3. **Install dependencies**:
```bash
sudo apt update
sudo apt install python3-pip python3-dev libpq-dev nginx git
```

4. **Clone repository**:
```bash
git clone your-repository-url
cd Data_V
```

5. **Set up virtual environment**:
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

6. **Configure environment variables** in `.env` file

7. **Run migrations**:
```bash
python manage.py migrate
python manage.py collectstatic --noinput
```

8. **Install and configure Gunicorn**:
```bash
pip install gunicorn
sudo nano /etc/systemd/system/gunicorn.service
```

9. **Configure Nginx**:
```bash
sudo nano /etc/nginx/sites-available/dataviz
sudo ln -s /etc/nginx/sites-available/dataviz /etc/nginx/sites-enabled
sudo nginx -t
sudo systemctl restart nginx
```

### Docker Deployment

1. **Build Docker image**:
```bash
docker build -t dataviz-dashboard .
```

2. **Run container**:
```bash
docker run -p 8000:8000 dataviz-dashboard
```

## Environment Variables

Create a `.env` file with the following variables:
```
DJANGO_SECRET_KEY=your-secret-key-here
DJANGO_DEBUG=True
DJANGO_ALLOWED_HOSTS=127.0.0.1,localhost
```

## Security Considerations

- Change `SECRET_KEY` in production
- Set `DEBUG=False` in production
- Configure proper `ALLOWED_HOSTS`
- Use HTTPS in production
- Regular security updates

## Troubleshooting

### Common Issues

1. **Module not found errors**: Ensure virtual environment is activated
2. **Database errors**: Run migrations: `python manage.py migrate`
3. **Static files not loading**: Run: `python manage.py collectstatic`
4. **Permission denied**: Check file permissions and ownership

### Logs
Check logs for debugging:
```bash
# Development
python manage.py runserver

# Production (Gunicorn)
tail -f /var/log/gunicorn/error.log
```