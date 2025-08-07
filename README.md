# 🔐 Secure Password Health Dashboard

A Django-based dashboard for monitoring and improving password hygiene and strength.

## Features
- Password strength checks
- Compromised password detection
- Encrypted storage
- Dashboard insights

## 🚀 Features
- Password strength checking (zxcvbn)
- Encrypted password storage
- Dashboard with password health score
- Compromised password check (HaveIBeenPwned)
- Password reuse & expiry detection
- Role-based access for users & orgs

## 🛠️ Tech Stack
- Django
- PostgreSQL or SQLite
- zxcvbn
- Cryptography
- Chart.js


## 📦 Recommended Third-party Packages
```bash
| Purpose                                    | Package                                                                                     |
| ------------------------------------------ | ------------------------------------------------------------------------------------------- |
| **User Auth & Roles**                      | `django-allauth` or `django-rest-auth` (for REST)                                           |
| **Password Strength**                      | `zxcvbn-python`                                                                             |
| **HIBP API**                               | `haveibeenpwned` or custom call to [Pwned Passwords API](https://haveibeenpwned.com/API/v3) |
| **Password Hashing & Encryption**          | `cryptography` (symmetric encryption), Django’s PBKDF2 for auth                             |
| **Dashboard UI**                           | `django-crispy-forms`, Charting with `Chart.js` or `Plotly`                                 |
| **Rate Limiting / Brute Force Protection** | `django-axes`                                                                               |
| **Logging/Audit Trails**                   | `django-simple-history` or custom model                                                     |

## 🧱 Django Project Structure
```bash
secure_pwd_dashboard/
├── manage.py
├── config/                  # Django settings, URLs
│   └── settings.py
├── users/                   # User registration, login, roles
│   ├── models.py
│   ├── views.py
├── passwords/               # Core password storage, analysis
│   ├── models.py
│   ├── views.py
│   ├── utils.py             # Strength checks, HIBP API
├── dashboard/               # UI and metrics
│   ├── views.py
│   ├── templates/
├── audits/                  # Logs of user actions
│   ├── models.py
│   ├── views.py


## Setup
```bash
git clone https://github.com/helooselassie/secure-password-dashboard.git
cd secure-password-dashboard
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env

