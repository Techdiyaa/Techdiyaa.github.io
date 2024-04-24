# Docker_IA_2
# Next.js and MongoDB application 
# Start from the Node.js 14 image
FROM node:14

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json (if exists) to the working directory
COPY package*.json ./

# Install npm dependencies based on the package.json file
RUN npm install

# Copy all files from the current directory (where the Dockerfile is located) into the working directory
COPY . .

# Expose port 3000 to allow external connections
EXPOSE 3000

# Set the default command to run when the container starts
CMD ["npm", "run", "dev"]  # This command runs the npm script named "dev"


# MongoDB
# Start from the latest mongo image
FROM mongo:latest

# Expose port 27017 to allow external connections
EXPOSE 27017

# Set the default command to run when the container starts
CMD ["mongod"]  # This command starts the MongoDB daemon (mongod)
