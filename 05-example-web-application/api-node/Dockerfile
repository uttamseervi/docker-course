# # 1️⃣ Use the official Node.js image as the base
# FROM node:18-alpine

# # 2️⃣ Set the working directory inside the container
# WORKDIR /app

# # 3️⃣ Copy package.json and package-lock.json first
# COPY package*.json ./

# # 4️⃣ Install dependencies (production only)
# RUN npm install --only=production

# # 5️⃣ Copy the rest of the project files
# COPY . .

# # 6️⃣ Set the correct working directory for your app
# WORKDIR /app/src

# # 7️⃣ Expose the port the app runs on
# EXPOSE 3000 9229  
# # 9229 is for debugging

# # 8️⃣ Start the application
# CMD ["node", "index.js"]


# hey, if you do like this every line in this docker file adds the new layer to this system so what we can do it (and) && it with the next command like the below one 
# FROM ubuntu

# RUN apt update 

# RUN apt install nodejs -y

FROM ubuntu

RUN apt update && apt install nodejs npm -y

COPY . . 
# the . . means copy the entire directory to this file 

RUN npm install 

CMD ["npm", "run", "dev"] # the last step is to add the command that will be executed at the runtime when we create a container