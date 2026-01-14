# MyShop - Django E-commerce Platform

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/)
[![Django Version](https://img.shields.io/badge/django-3.2%2B-green)](https://www.djangoproject.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**MyShop** is a full-featured e-commerce application built with Python and Django. It provides a seamless shopping experience from product browsing to checkout, featuring a recommendation engine and multi-language support.

---

## 🚀 Features

* **Product Catalog**: Browse products organized by categories with high-quality images and descriptions.
* **Shopping Cart**: A session-based shopping cart allowing users to add, update, and remove products.
* **Order Management**: Secure checkout process with order persistence in the database.
* **Internationalization (i18n)**: Support for multiple languages (e.g., English, Spanish) to reach a global audience.
* **Recommendation Engine**: Intelligent "users who bought this also bought" suggestions powered by **Redis**.
* **Payment Integration**: Secure payment processing integrated with **Stripe**.
* **PDF Invoices**: Automatic generation of PDF invoices for customers upon successful order completion.
* **Asynchronous Tasks**: Background email notifications handled by **Celery** and **RabbitMQ**.

---

## 🛠 Tech Stack

| Component | Technology |
| :--- | :--- |
| **Backend** | Django (Python) |
| **Database** | PostgreSQL / SQLite |
| **Caching/NoSQL** | Redis |
| **Task Queue** | Celery & RabbitMQ |
| **Payment Gateway** | Stripe API |
| **Frontend** | Bootstrap, jQuery, CSS3 |

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
* Python 3.8+
* Redis Server
* RabbitMQ (for Celery background tasks)
* A Stripe account for API keys

---

## ⚙️ Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/satish24011993/myshop.git](https://github.com/satish24011993/myshop.git)
    cd myshop
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    python -m venv venv
    # On Windows:
    venv\Scripts\activate
    # On macOS/Linux:
    source venv/bin/activate
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Configure Environment Variables:**
    Create a `.env` file in the root directory and add your Stripe keys:
    ```env
    STRIPE_PUBLISHABLE_KEY=your_pub_key
    STRIPE_SECRET_KEY=your_sec_key
    STRIPE_WEBHOOK_SECRET=your_webhook_secret
    ```

5.  **Apply migrations:**
    ```bash
    python manage.py migrate
    ```

6.  **Create a superuser:**
    ```bash
    python manage.py createsuperuser
    ```

---

## 🏃 Running the Application

1.  **Start Redis server:**
    ```bash
    redis-server
    ```

2.  **Start Celery worker** (in a new terminal):
    ```bash
    celery -A myshop worker -l info
    ```

3.  **Start the Django server:**
    ```bash
    python manage.py runserver
    ```

Navigate to `http://127.0.0.1:8000/` to view the site.

---

## 📂 Project Structure
```text
myshop/
├── cart/           # Shopping cart logic
├── orders/         # Order processing and PDF generation
├── payment/        # Stripe integration
├── shop/           # Product catalog and core logic
├── myshop/         # Project configuration (settings, URLs)
├── static/         # CSS, JS, and Images
├── templates/      # HTML Templates
└── manage.py
```

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. **Fork** the Project
2. **Create** your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your Changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the Branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

## 📧 Contact

**Satish Kurakula** 📩 Email: [satishkurakula073@gmail.com](mailto:satishkurakula073@gmail.com)  
🔗 Project Link: [https://github.com/satish24011993/myshop](https://github.com/satish24011993/myshop)

---

## 🛠 Future Roadmap / API Documentation

* [ ] Add Swagger/Redoc for API documentation.
* [ ] Integrate unit tests for the recommendation engine.
* [ ] Implement Docker containerization for easier deployment.
