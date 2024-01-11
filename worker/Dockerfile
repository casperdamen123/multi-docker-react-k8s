# Set base image
FROM node:alpine

# Working directory
WORKDIR /APP

# Copy requirements
COPY ./package.json ./

# Install npm
RUN npm install

# Copy the rest of application code
COPY ./ ./

# Start app
CMD ["npm", "run", "dev"]