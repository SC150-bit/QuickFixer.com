FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

# Declare the ARG and set ENV before running build
ARG MONGO_URI
ENV MONGO_URI=$MONGO_URI

RUN npm run build

EXPOSE 3000
CMD ["npm", "start"]
