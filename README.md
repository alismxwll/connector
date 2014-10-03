[![Code Climate](https://codeclimate.com/github/factor-io/connector/badges/gpa.svg)](https://codeclimate.com/github/factor-io/connector)
[![Test Coverage](https://codeclimate.com/github/factor-io/connector/badges/coverage.svg)](https://codeclimate.com/github/factor-io/connector)
[![Dependency Status](https://gemnasium.com/factor-io/connector.svg)](https://gemnasium.com/factor-io/connector)
[![Build Status](https://travis-ci.org/factor-io/connector.svg)](https://travis-ci.org/factor-io/connector)
# Factor.io Connector
The Factor.io Connector is a [Sinatra](http://www.sinatrarb.com/) server for hosting integrations with 3rd party services. It provides a single interface for the runtime to all the integrated services. When you run the [Factor.io Server](https://github.com/factor-io/factor) (`factor s`) it uses WebSockets to connect to this Connector.

## Integrations
There is no code in this server for defining the third party services. Each of the integrations like [Github](https://github.com/factor-io/connector-github), [Heroku](https://github.com/factor-io/connector-heroku), [Rackspace](https://github.com/factor-io/connector-rackspace), [Hipchat](https://github.com/factor-io/connector-hipchat) are defined in separate gems, and they use the [factor-connector-api gem](https://github.com/factor-io/connector-api)  as a common library to define those integrations.

### Load a new integration
1. Add the gem containing the integration to the [Gemfile](https://github.com/factor-io/connector/blob/master/Gemfile).
2. Add the appropriate `require` statement in [init.rb](https://github.com/factor-io/connector/blob/master/init.rb).

## Running
### Localhost
    git clone git@github.com:factor-io/connector
    bundle install
    bundle exec rackup

### Heroku

[Click here!](https://heroku.com/deploy) Yup, it's that easy.

## Running Tests
To execute all the tests just run:

    rake
