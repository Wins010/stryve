FROM node:18-bullseye

WORKDIR /app

# Copy only the lock + package files first (for caching)
COPY package.json package-lock.json ./

# Copy the rest of the frontend files
COPY . .

RUN npm install -g expo-cli && npm install

EXPOSE 8081

CMD ["npx", "expo", "start", "--lan", "--non-interactive"]