# Use an official Node.js runtime as the base image
FROM node:12

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Install nodemon for development
RUN npm install --save-dev nodemon

# Copy the rest of the application code
COPY . .

# Set environment variable
ENV PORT=8080

# Expose the port the app runs on
EXPOSE 8080

# Start the application with nodemon for development
CMD ["npx", "nodemon", "index.js"]
