FROM node:alpine as build
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build --prod


FROM nginx:alpine
COPY --from=build app/dist/electric-equipment-ui usr/share/nginx/html
EXPOSE 80
