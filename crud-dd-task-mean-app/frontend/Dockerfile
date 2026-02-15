# ---------- Stage 1: Build Angular App ----------
FROM node:18 as build

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

RUN npm run build --prod

# ---------- Stage 2: Serve using Nginx ----------
FROM nginx:alpine

# Copy Angular build files to nginx
COPY --from=build /app/dist/angular-15-crud/ /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]


