FROM node:lts-alpine

ENV PORT 3000

# Create app directory
RUN mkdir -p /app
WORKDIR /app

# Install app dependencies
COPY package*.json ./
RUN npm install

# Bundle app source
COPY ./ ./

RUN npm run build
EXPOSE 3000

CMD [ "npm", "start" ]