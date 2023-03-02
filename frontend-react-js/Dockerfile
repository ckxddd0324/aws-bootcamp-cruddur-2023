FROM node:16.18

WORKDIR /frontend-react-js

ENV PORT=3000
COPY . .

COPY package.json package.json
RUN npm i
RUN npm install react-scripts


EXPOSE ${PORT}
CMD ["npm", "start"]