# Base python
FROM python:3.8

# Set the working directory to /app
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt .

# Install the packages defined in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code into the container
COPY . .

# Run the init_db.py script to initialize the database
RUN python init_db.py

# Expose port 3111 for the application
EXPOSE 3111

# Start the application when the container starts
CMD ["python", "app.py"]
