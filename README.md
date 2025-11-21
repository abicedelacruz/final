ABIC Manpower - Payroll App (Minimal Flask)
===========================================

What this contains
- Flask app with SQLite database
- Admin dashboard: add/remove employees, create payrolls, view payroll history
- Auto-generate username/password for each employee (password hashed in DB)
- Employee login to view their own payslips only
- Payslip layout (prettified with Bootstrap)
- Payroll computation using the formulas you provided for Mali Lending Corp (best-effort)
- Ability to load previous payroll inputs when creating a new payroll for an employee

How to run locally
1. Ensure Python 3.10+ is installed.
2. Create virtualenv and install requirements:
   python -m venv venv
   source venv/bin/activate  (or venv\Scripts\activate on Windows)
   pip install -r requirements.txt
3. Initialize DB (first run will auto-create db with an admin user):
   flask --app app.py run --host=0.0.0.0 --port=5000
4. Default admin login: username: admin@example.com password: AdminPass123
   Please change it immediately from the Admin > Settings page (simple implementation).

Deployment notes
- For remote 24/7 hosting you can deploy to Render, Fly.io, Railway, or use a VPS.
- For quick remote exposure you can use ngrok for development (not production).

Project files description:
- app.py: main Flask app
- templates/: Jinja2 HTML templates
- static/: CSS and simple client assets
- abic_payroll.db: SQLite DB (created at first run)
