# Step 1: Use an official Node.js image
FROM node:18-alpine

# Step 2: Set the working directory inside the container
WORKDIR /app

# Step 3: Copy dependency files first and install
COPY package*.json ./
RUN npm install

# Step 4: Copy the rest of the source code
COPY . .

# Step 5: Build the app for production
RUN npm run build

# Step 6: Expose the Vite default dev port
EXPOSE 5173

# Step 7: Start the app (development mode)
CMD ["npm", "run", "dev"]
