FROM serversideup/php:8.2-fpm-nginx

# Set the document root for Nginx to Laravel's public directory
ENV DOCUMENT_ROOT=/var/www/html/public

# Set system environment variables
ENV APP_ENV=production
ENV APP_DEBUG=true
ENV APP_KEY="base64:Dymg1P6E1hH3Dq6w8G6kR9Z0kE4xO6wB1tP9qL4vF4g="
ENV DB_CONNECTION=sqlite
ENV DB_DATABASE=/var/www/html/database/database.sqlite

# Copy application files and set ownership to www-data
COPY --chown=www-data:www-data . /var/www/html

# Switch to root to ensure permissions during build
USER root

# Install composer dependencies
RUN composer install --no-dev --optimize-autoloader --no-interaction

# Create and initialize SQLite database during build
RUN touch database/database.sqlite && \
    php artisan migrate --force && \
    php artisan db:seed --force && \
    chown -R www-data:www-data /var/www/html

# Switch back to www-data for runtime
USER www-data
