# Base image
FROM node:14-alpine

# Set working directory
WORKDIR /app

# add `/app/node_modules/.bin` to $PATH
ENV PATH /app/node_modules/.bin:$PATH

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy app files
COPY . .

ENV PORT=5001

# Expose port
EXPOSE 5001

# start app
CMD ["npm", "run", "dev"]
