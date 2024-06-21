FROM node:15 as builder

# Set working directory
WORKDIR /app

# Copy package files
COPY package.json /app/package.json
COPY package-lock.json /app/package-lock.json

# Same as npm install
RUN npm ci

COPY . /app

ENV CI=true
ENV PORT=3000

EXPOSE 3000

CMD [ "npm", "start" ]