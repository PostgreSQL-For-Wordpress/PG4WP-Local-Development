
# PG4WP Local Development Environment

__:warning:WARNING:warning:__ This is only meant as a local development environment.   
__Please do not use this as a reference configuration for a production deployment__



https://github.com/PostgreSQL-For-Wordpress/PG4WP-Local-Development/assets/3284147/f2c31c2b-313f-4647-b828-325d91ed6f9c




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
``` bash
wp --allow-root core install --url=http://wordpress.localhost --title="Wordpress Local Dev" --admin_user=root --admin_email="root@example.com" --admin_password=secret
```

To see your site  
Navigate to http://wordpress.localhost  

To log in and view the dashboard using username root and password "secret"  
Navigate to http://wordpress.localhost/wp-admin  
