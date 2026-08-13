
FROM node:22-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

# ... your previous setup steps (like COPY and npm install) are above here

# 1. Compile the React/Vite assets into a production folder
RUN npm run build

# 2. Expose the deployment network port
EXPOSE 10000

# 3. Start the production asset preview server
CMD ["npm", "run", "preview"]

