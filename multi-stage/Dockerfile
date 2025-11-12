# Stage 1: Build
FROM node:14 as build-stage
WORKDIR /app/multi-stage
COPY package*.json ./
RUN npm install
COPY . .
# Add the following line if there's a build step for the app
# RUN npm run build

# Stage 2: Run
FROM node:14-alpine
WORKDIR /app/multi-stage
COPY --from=build-stage /app/multi-stage .
EXPOSE 3000
ENV NODE_ENV=production
CMD ["node", "Node.js"]