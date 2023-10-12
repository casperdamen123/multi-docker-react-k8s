FROM node:alpine

# Set working directory
WORKDIR /app

# Copy package.json to working directory
COPY package.json .
RUN npm install
COPY . .

CMD ["npm", "start"]