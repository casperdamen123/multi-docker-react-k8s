# Set base image
FROM node:14.14.0-alpine

# Working directory
WORKDIR /APP

# Copy requirements
COPY ./package.json ./

# Install npm
RUN npm install

# Copy rest of application code
COPY ./ ./

# Start app
CMD ["npm", "run", "start"]