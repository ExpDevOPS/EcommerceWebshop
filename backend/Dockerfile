# Use an official Python runtime as a parent image
FROM python:3.10

# Set the working directory inside the container
WORKDIR /app

# Copy requirements.txt from the root folder into the /app directory
COPY ../requirements.txt /app/

# Debugging step to verify files are copied
RUN ls -l /app

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the files from the root folder into the container
COPY ../manage.py /app/
COPY ../backend /app/backend

# Expose the port the app runs on
EXPOSE 8000

# Run the Django application
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]