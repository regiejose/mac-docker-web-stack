# Features

- `Nginx` with exposed awesome vhost support
- `MariaDB` with data mounted on the folder (`say goodbye to missing DBs`)
- `Need to destroy your Docker stack, you keep all data, even your Databases`
- `Redis` with data mounted on the folder
- `PHP 7` with FPM
    Create instance from scratch for about 10 - 15 mins
    Up or halt the instance almost instantly (well 5 secs to be exact)

This stack was based from the [Laradock project](https://github.com/laradock/laradock).

# Requirements

- `Docker` v17.03.1-ce or higher
- `docker-compose` v1.12 or higher

# Usage

This Docker stack includes easy commands, so you do not need to remember the
commands to run or reload things.

If you edit vhosts, for example, you need to reload nginx. If you edit mariadb
settings, then you need to reload it.

- `./bin/start` Starts the stack
- `./bin/stop` Stops the stack
- `./bin/reload` Reloads everything, but does not recreate it
- `./bin/reload nginx` Recreates nginx instance
- `./bin/reload <service_name>` Recreates any service instance
- `./bin/mysql` Connect to your MariaDb Service

# FAQ

#### How does Docker mounting work ?
> On the `.env` file there is a `APPLICATION` variable which you can set manualy to any folder.
> This gets mounted to the Docker workspace to the folder `/var/www`

#### How to add new Nginx vhost ?

> Simply go to `./services/nginx/sites` as this folder gets mounted on the conf.d of nginx directly. After adding new sites, simply run `./bin/reload`

#### Configured vhost already but still the site cannot be reached ?

> Make sure to add your server name(s) on `etc/hosts` file (may require sudo privilege)

# Warranties

- This stack was built on `macOS Sierra` v10.12.5. Experience may vary on other operating systems.