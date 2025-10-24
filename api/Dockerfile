# Use latest PHP FPM (8.3) official image
FROM php:8.4-fpm

# Set working directory
WORKDIR /var/www/api

# Install system dependencies
RUN apt-get update && apt-get install -y \
	git \
	unzip \
	libicu-dev \
	libonig-dev \
	libxml2-dev \
	zip \
	curl \
	supervisor \
	libzip-dev \
	zlib1g-dev \
	&& rm -rf /var/lib/apt/lists/*

# Install PHP extensions commonly used by Symfony
RUN docker-php-ext-install pdo pdo_mysql intl mbstring zip xml opcache

# Install Composer
COPY --from=composer:2.6 /usr/bin/composer /usr/bin/composer

# Install Symfony CLI (optional, useful for local dev)
RUN curl -sS https://get.symfony.com/cli/installer | bash \
	&& mv /root/.symfony*/bin/symfony /usr/local/bin/symfony

# Copy Symfony application into container
COPY . /var/www/api

# Set permissions (Symfony requires write access for var/cache and var/log)
RUN chown -R www-data:www-data /var/www/api/var /var/www/api/vendor
RUN chmod -R 775 /var/www/api/var /var/www/api/vendor

# Expose port 9000 for FPM
EXPOSE 9000

# Run PHP-FPM
CMD ["php-fpm"]

