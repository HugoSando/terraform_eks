FROM node:20.11.1-alpine3.19

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
COPY package.json ./
RUN npm install

# Bundle app source
COPY . .

RUN npm run build

EXPOSE 3000
ENTRYPOINT [ "npm", "run", "preview", "--", "--host", "0.0.0.0"]
