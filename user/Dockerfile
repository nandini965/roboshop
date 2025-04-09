
FROM             node
RUN              mkdir /app
WORKDIR          /app
COPY             server.js .
COPY             . .
ADD              https://truststore.pki.rds.amazonaws.com/global/global-bundle.pem /app/rds-combined-ca-bundle.pem
RUN               npm install
EXPOSE 8080
CMD ["node", "server.js"]
