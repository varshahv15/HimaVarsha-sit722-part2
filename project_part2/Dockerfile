
# Using official Python runtime as a parent image
FROM python:3.9-slim

# working directory in the container
WORKDIR /app

# Copying the requirements file into the container
COPY book_catalog/requirements.txt ./

# Installing the Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copying the rest of the application code into the container
COPY book_catalog/ ./

# Exposing the application port
EXPOSE 8000

# Defining the command to run the application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]


