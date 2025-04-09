FROM             node
RUN              mkdir /app
WORKDIR          /app
COPY             server.js .
COPY             . .
ADD         mongodb://username:password@mongodb:27017/catalogue?tls=true&replicaSet=rs0&readPreference=secondaryPreferred&retryWrites=false
RUN              npm install
EXPOSE 8080
CMD ["node", "server.js"]
