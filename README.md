
# PG4WP Local Development Environment

## Prerequisties
    Install docker-compose or podman-compose + docker dependencies

## Bundled Dependencies
    Postgres 14
    PHP FPM with required extensions
    NGINX


## Getting Started
Clone this repo 
git clone git@github.com:PostgreSQL-For-Wordpress/PG4WP-Local-Development.git

docker-compose up -d
docker-compose exec phpfpm /bin/sh
wp --allow-root core install --url=http://wordpress.localhost --title="Wordpress Local Dev" --admin_user=root --admin_email="root@example.com" --admin_password=secret

Navigate to http://wordpress.localhost to see your site

Navigate to http://wordpress.localhost/wp-admin to log in and view the dashboard