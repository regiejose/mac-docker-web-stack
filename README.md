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

# Warranties

- This stack was built on `macOS Sierra` v10.12.5. Experience may vary on other operating systems.