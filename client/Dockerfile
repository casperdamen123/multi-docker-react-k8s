# Set builder image
FROM node:16-alpine as builder

# Working directory
WORKDIR /APP

# Copy requirements
COPY ./package.json ./

# Install npm
RUN npm install

# Copy rest of application code
COPY ./ ./

# Start the app
RUN npm run build

# Set base image
FROM nginx  

# Expose port 3000
EXPOSE 3000

# Copy configuration files
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf

# Copy build files
COPY --from=builder /APP/build /usr/share/nginx/html