# Backend Laravel — PHP + Composer
# El código se monta con volumen en docker-compose; no se copia aquí.

FROM php:8.2-cli

# Dependencias del sistema
RUN apt-get update && apt-get install -y \
    git \
    unzip \
    libzip-dev \
    libpng-dev \
    libonig-dev \
    && rm -rf /var/lib/apt/lists/*

# Extensiones PHP que Laravel suele usar
RUN docker-php-ext-install pdo_mysql zip exif pcntl bcmath gd

# Composer
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

WORKDIR /var/www

# Por defecto el compose define el command; aquí solo un fallback
CMD ["php", "artisan", "serve", "--host=0.0.0.0", "--port=8000"]
