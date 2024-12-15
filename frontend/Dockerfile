# Use the official Angular image
FROM node:14-alpine

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json first
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the Angular app code
COPY . .

# Expose the port Angular runs on
EXPOSE 4200

# Start the Angular app
CMD ["ng", "serve", "--host", "0.0.0.0", "--port", "4200"]
