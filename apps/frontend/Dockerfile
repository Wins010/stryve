FROM node:18-bullseye

WORKDIR /app

# Copy lock + package files first
COPY package.json package-lock.json ./

# Install Expo CLI **and ngrok** globally first
RUN npm install -g expo-cli @expo/ngrok

# Install project dependencies
RUN npm install

# Copy the rest of the code
COPY . .

EXPOSE 8081

# CI=0 enables QR code; use tunnel mode automatically
CMD ["sh", "-c", "CI=0 npx expo start --lan"]
#changed from --tunnel to --lan 15/12/2025 6:09 AM @Sult9n0-0