# Use official Node image
FROM node:18

# Create app directory inside container
WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all backend source code
COPY . .

# Expose backend port
EXPOSE 8080

# Start backend server
CMD ["node", "server.js"]


