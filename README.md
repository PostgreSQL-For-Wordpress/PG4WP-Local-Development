
# PG4WP Local Development Environment

__:warning:WARNING:warning:__ This is only meant as a local development environment.   
__Please do not use this as a reference configuration for a production deployment__

## Prerequisties
    Install docker-compose or podman-compose + docker dependencies

## Bundled Dependencies
    Postgres 14
    PHP FPM with required extensions
    NGINX


## Getting Started
Clone this repo 
`git clone --recurse-submodules git@github.com:PostgreSQL-For-Wordpress/PG4WP-Local-Development.git`

Start the environment  
`docker-compose up -d`

Enter the php-fpm container  
`docker-compose exec phpfpm /bin/sh`

Perform the 1 time install  
`wp --allow-root core install --url=http://wordpress.localhost --title="Wordpress Local Dev" --admin_user=root --admin_email="root@example.com" --admin_password=secret`

Navigate to http://wordpress.localhost to see your site

Navigate to http://wordpress.localhost/wp-admin to log in and view the dashboard using username root and password "secret"