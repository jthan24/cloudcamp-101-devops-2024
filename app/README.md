
export FLASK_APP=main.py
python -m flask run --port 8080 --host 0.0.0.0


docker build --tag python-docker .
docker run -d -p 80:8080 --name python-docker python-docker

