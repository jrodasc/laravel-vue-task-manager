# Frontend Vue — Node para desarrollo con Vite
# El código se monta con volumen en docker-compose; no se copia aquí.

FROM node:20-alpine

WORKDIR /app

# Por defecto el compose define el command; aquí solo un fallback
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
