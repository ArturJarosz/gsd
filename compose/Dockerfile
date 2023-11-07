ARG port=8080

# Base image
FROM python:alpine

# Copy app, templates and views
COPY . /app

# Set working directory for subsequent commands
WORKDIR /app

# Install dependencies
RUN pip install -r requirements.txt

RUN echo "exposing port"
EXPOSE $port

# Command to run when container starts
ENTRYPOINT ["python", "app/app.py"]
