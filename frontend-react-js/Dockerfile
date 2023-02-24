FROM node:16.18

WORKDIR /frontend-react-js

ENV PORT=3000

COPY package.json package.json
RUN npm install react-scripts
RUN npm i

COPY . .

EXPOSE ${PORT}
CMD ["npm", "start"]