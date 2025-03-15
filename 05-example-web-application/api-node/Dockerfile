# 1️⃣ Use the official Node.js image as the base
FROM node:18-alpine

# 2️⃣ Set the working directory inside the container
WORKDIR /app

# 3️⃣ Copy package.json and package-lock.json first
COPY package*.json ./

# 4️⃣ Install dependencies (production only)
RUN npm install --only=production

# 5️⃣ Copy the rest of the project files
COPY . .

# 6️⃣ Set the correct working directory for your app
WORKDIR /app/src

# 7️⃣ Expose the port the app runs on
EXPOSE 3000 9229  
# 9229 is for debugging

# 8️⃣ Start the application
CMD ["node", "index.js"]
