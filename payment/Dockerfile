# Step 1: Use an official Python image from the Docker Hub
FROM python:3.9-slim

# Step 2: Install system dependencies required for building packages
RUN apt-get update && apt-get install -y \
    build-essential \
    && rm -rf /var/lib/apt/lists/*  # Clean up to reduce image size


# Step 4: Copy the requirements file into the container
COPY requirements.txt .

# Step 5: Install the Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Step 6: Copy the rest of the application code into the container
COPY . .

# Step 7: Define the command to run the application
CMD ["python", "payment.py"]

# Optionally, expose a port if your app listens on one
EXPOSE 5000

