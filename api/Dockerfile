FROM node:17-alpine

RUN npm install -g nodemon

WORKDIR /app

# copying these 2 files inside IMAGE
COPY package.json package-lock.json .

RUN npm install

# copying everything inside /app which in turn is inside CONTAINER. Notice the difference b/w this copy command and json-files-copy command
COPY . .

# RUN node index.js
# the above RUN command is not used bcoz RUN command runs commands at build time of the image, 
# where as the below command 'CMD ['node', 'index.js']' runs commands at run time of the container

EXPOSE 4000

CMD ["npm", "run", "dev"]