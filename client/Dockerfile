# Use Node.js LTS Alpine as base image
FROM node:lts-alpine

# Set working directory
WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy rest of the application
COPY . .

# Build the application
RUN npm run build

# Install serve
RUN npm install -g serve

# Expose port 3000
EXPOSE 3000

# Start the server
CMD ["serve", "-s", "build", "-l", "3000"]