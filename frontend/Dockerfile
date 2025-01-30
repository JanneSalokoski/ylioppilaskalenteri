FROM node:18-alpine

# Install elm and required js/ts tooling
WORKDIR /usr/src/app
COPY package.json package-lock.json ./
RUN npm install

# Copy source code
COPY . .

# expose port 3000
EXPOSE 3000

CMD ["npx", "elm-live", "src/Main.elm", "--hot", "--dir=static", "--port=3000", "--", "--output=static/main.js"]
