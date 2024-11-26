# Use Node.js base image
FROM node:lts-alpine

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all other server files
COPY . .

# Expose the server port
EXPOSE 9000

# Start the server
CMD ["npm", "start"]
