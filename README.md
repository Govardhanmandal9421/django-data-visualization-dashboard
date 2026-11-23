# 📊 Django Dynamic Data Visualization Dashboard

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-5.x-092E20?style=for-the-badge&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Govardhan_Mandal-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/govardhan-mandal-268121440/)

A full-stack Django web application designed for automated statistical data generation, relational persistence, and dynamic multi-chart visualization analytics.

---

## 🖼️ Dashboard Preview

![Dashboard Preview](dashboard_image.jpeg)

---

## 🚀 Key Features

* 📊 **Multi-Chart Analytics Suite:** Generates dynamic statistical plots including Bar charts, Scatter plots, Histograms, Box plots, Violin plots, and Line charts.
* 📋 **Paginated Data Explorer:** Responsive data table with server-side pagination (10 records/page) and rapid search filters.
* 🤖 **Automated Synthetic Data Generator:** Integrated `Faker` engine that populates relational SQLite/PostgreSQL schemas with thousands of realistic records on demand.
* 🎨 **Modern Cyberpunk UI:** Built with responsive CSS Grid, glassmorphic cards, smooth interactive transitions, and mobile viewport adaptability.
* 🐳 **Docker & Compose Ready:** Containerized setup for deterministic local or cloud deployments.

---

## 🛠️ Technology Stack

* **Backend:** Python 3.x, Django Web Framework (MVC Architecture)
* **Database:** SQLite3 / PostgreSQL with Django ORM
* **Data Synthesis & Computation:** Faker, Pandas, NumPy
* **Visualization Libraries:** Matplotlib, Seaborn, Plotly
* **DevOps:** Docker, Docker Compose, Gunicorn

---

## 💻 Installation & Quickstart

```bash
# 1. Clone the repository
git clone https://github.com/Govardhanmandal9421/django-data-visualization-dashboard.git
cd django-data-visualization-dashboard

# 2. Create and activate virtual environment
python -m venv venv
# On Windows:
venv\Scripts\activate
# On Linux/macOS:
source venv/bin/activate

# 3. Install dependencies & run migrations
pip install -r requirements.txt  # or: pip install django faker pandas matplotlib seaborn
python manage.py migrate

# 4. Launch local development server
python manage.py runserver
```

Open `http://127.0.0.1:8000` in your web browser.

---

## 👨‍💻 Author & Connect

* **Developer:** Govardhan Mandal
* **Portfolio:** [govardhanmandal9421.github.io](https://govardhanmandal9421.github.io)
* **LinkedIn:** [linkedin.com/in/govardhan-mandal-268121440](https://www.linkedin.com/in/govardhan-mandal-268121440/)
* **GitHub:** [github.com/Govardhanmandal9421](https://github.com/Govardhanmandal9421)
* **Email:** [g.s.mandal433@gmail.com](mailto:g.s.mandal433@gmail.com)
