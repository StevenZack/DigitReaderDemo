FROM python:3.10.12-slim

WORKDIR /app

COPY api.py .
COPY handwriting.keras .
COPY index.html .

RUN pip install tensorflow numpy mnist keras fastapi "uvicorn[standard]" Pillow

EXPOSE 8080
CMD [ "python3","api.py" ]