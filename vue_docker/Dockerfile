FROM node:latest as vue
WORKDIR /usr/app
COPY package*.json ./
copy . .
RUN npm install && npm run build 



FROM nginx:1.15 
WORKDIR /usr/share/nginx/html
copy --from=vue /usr/app/dist .

