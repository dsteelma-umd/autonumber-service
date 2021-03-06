# autonumber-service

Rails implementation of the Autonumber service.

This is a reimplementation of the Autonumber service from the [Grails Services][1] app.

## Quick Start

Requires:

* Ruby 2.2.4
* Bundler

```
git clone git@github.com:umd-lib/autonumber-service
cd autonumber-service
bundle install --without production --path vendor
rails server
```

<http://localhost:3000/auto_numbers>

## Production Environment Configuration

Requires:

* Postgres client to be installed (on RedHat, the "postgresql" and 
"postgresql-devel" packages)

The application uses the "dotenv" gem to configure the production environment.
The gem expects a ".env" file in the root directory to contain the environment
variables that are provided to Ruby. A sample "env_example" file has been
provided to assist with this process. Simply copy the "env_example" file to
".env" and fill out the parameters as appropriate.

The configured .env file should _not_ be checked into the Git repository, as it
contains credential information.


[1]: https://github.com/umd-lib/grails-services
