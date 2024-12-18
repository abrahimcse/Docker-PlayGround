# Stage 1: Build the React application
FROM node:14-alpine as builder

# Set the working directory
WORKDIR /app

# Install build dependencies for Alpine
RUN apk --update add libtool automake autoconf nasm gcc make g++ zlib-dev

# Copy package.json and package-lock.json
COPY package*.json  ./

# Install dependencies
RUN npm install

# Copy the source code
COPY . .

# Build the React app for production
RUN npm run build

# Stage 2: Serve the built app using Nginx
FROM nginx

# Copy the build output from the builder stage to Nginx's web directory
COPY --from=builder /app/public /user/share/nginx/html
