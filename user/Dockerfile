FROM   node:20
WORKDIR /app
COPY    . ./
RUN npm install
EXPOSE 8080
CMD ["node", "server.js"]

FROM             node
RUN              mkdir /app
WORKDIR          /app
COPY             server.js .
COPY             node_modules node_modules
ADD              https://truststore.pki.rds.amazonaws.com/global/global-bundle.pem /app/rds-combined-ca-bundle.pem
RUN npm install
EXPOSE 8080
CMD ["node", "server.js"]
