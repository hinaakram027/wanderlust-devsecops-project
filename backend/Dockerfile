# Stage 1
FROM node:21 As backend-builder
WORKDIR /app
COPY . .
RUN npm 1
# Stage 2
FROM node:21-slim
WORKDIR /app
COPY --from-backend-builder /app .
COPY .env.docker .env
EXPOSE 5000
CMD ["npm", "start"]
