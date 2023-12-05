FROM python:3-buster
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
CMD ["python", "/app/app.py"]
#with the last copy command we can make changes to our workdir and docker will not run again the previous commands (if we won't change the requirements)
COPY . .