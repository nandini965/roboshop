FROM node:20
ENV INSTANA_AUTO_PROFILE true
WORKDIR /app
COPY . ./
RUN npm install
EXPOSE 8080
CMD ["node", "server.js"]