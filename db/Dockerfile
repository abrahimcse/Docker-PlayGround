# Use the official MongoDB image
FROM mongo:4.4

# Set the working directory in the container
WORKDIR /data/db

# Expose MongoDB default port
EXPOSE 27017

# Optionally, set environment variables for MongoDB configuration
ENV MONGO_INITDB_ROOT_USERNAME=root
ENV MONGO_INITDB_ROOT_PASSWORD=password
ENV MONGO_INITDB_DATABASE=mydatabase

# Optional: Copy any configuration files if needed
# COPY mongo.conf /etc/mongo.conf

# Start MongoDB
CMD ["mongod"]
