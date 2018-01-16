# docker-php-fpm-with-mail
PHP FPM docker with mail support (based on Alpine)

## Docker compare example

```yaml
version: '3'

services:
  phpfpm:
    image: 'martinvw/php-fpm-with-mail'
    restart: always
    volumes:
      - './msmtprc:/etc/msmtprc'
      - 'website_sources:/var/www/html:ro'

volumes:
  website_sources:
    driver: local
```  
