# Use Node.js with Alpine Linux as the base image (lightweight version)
FROM node:alpine

# Set the working directory inside the container to /app
WORKDIR /app

# Copy package.json file to the working directory
# This is done separately to leverage Docker layer caching
COPY ./package.json .

# Install dependencies listed in package.json
RUN npm install

# Copy all remaining files from the current directory to the container
COPY . .

# Define the default command to run when the container starts
CMD ["npm", "run", "host"]