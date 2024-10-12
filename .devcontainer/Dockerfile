FROM mcr.microsoft.com/devcontainers/python:1-3.12-bullseye

WORKDIR /app

COPY . .

RUN pip install -r requirements.txt

EXPOSE 8501

HEALTHCHECK CMD curl --fail http://localhost:8501/_stcore/health

ENTRYPOINT ["streamlit", "run", "app/main.py", "--server.port=8501", "--server.address=0.0.0.0"]