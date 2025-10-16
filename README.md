# Flask Project

Simple Flask app served by Gunicorn and managed by systemd.

## Run locally
# In app/
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py

## Service (systemd)
sudo cp systemd/flask-app.service /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl enable --now flask-app

