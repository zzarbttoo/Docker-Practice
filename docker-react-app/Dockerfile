FROM node:alpine as builder
WORKDIR /usr/src/app
COPY home/zzarbttoo/Docker-Practice/docker-react-app/package.json ./
RUN npm install
COPY home/zzarbttoo/Docker-Practice/docker-react-app/ ./
RUN npm run build 

FROM nginx 
EXPOSE 80 
COPY --from=builder /usr/src/app/build /usr/share/nginx/html

