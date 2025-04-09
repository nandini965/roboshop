FROM             node
RUN              mkdir /app
WORKDIR          /app
COPY             server.js .
COPY              . .
RUN              npm install
EXPOSE           8080
CMD              ["node", "server.js"]
