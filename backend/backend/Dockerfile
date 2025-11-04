# Use official Node.js LTS image
FROM node:18-slim

# Create app directory
WORKDIR /usr/src/app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install --production

# Copy the rest of the application source
COPY . .

# Ensure uploads folder exists
RUN mkdir -p src/uploads

# Expose port (Render or Docker will map this)
EXPOSE 4000

# Start the application
CMD ["node", "src/index.js"]
