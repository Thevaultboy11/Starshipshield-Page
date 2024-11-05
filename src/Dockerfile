# Use an official Node.js runtime as the base image
FROM node:18

# Set the working directory in the container to /app
WORKDIR /app

# Copy package.json and package-lock.json to install dependencies
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install --force

# Copy the rest of the application code into the container
COPY . .

# Build the application for production
RUN npm run build

# Expose the port Astro uses
EXPOSE 3000

# Define the command to run the application
CMD ["npm", "run", "start"]
