FROM node:17-alpine

WORKDIR /app

COPY . .

RUN npm install

# RUN node index.js
# the above RUN command is not used bcoz RUN command runs commands at build time of the image, 
# where as the below command 'CMD ['node', 'index.js']' runs commands at run time of the container

EXPOSE 4000

CMD ["node", "index.js"]