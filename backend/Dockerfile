# Use the official Node.js image
FROM node:14-alpine

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json first
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on
# EXPOSE 3000

# Start the app
# CMD ["node", "index.js"]
CMD npm run start