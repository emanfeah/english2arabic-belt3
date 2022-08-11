FROM node:10-alpine
ENV NODE_ENV=production
ENV API_ENDPOINT=./api
# Create app directory
WORKDIR /usr/src/app
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install --production --silent && mv node_modules ../
COPY . .
EXPOSE 80
RUN chown -R node /usr/src/app
USER node
CMD ["node", "index.js"]


