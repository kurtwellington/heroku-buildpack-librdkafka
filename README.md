# librdkafka buildpack

This buildpack compiles librdkafka for use with [confluent-kafka-python](https://github.com/confluentinc/confluent-kafka-python).

## Usage

Use with [multi-buildpacks](https://devcenter.heroku.com/articles/using-multiple-buildpacks-for-an-app).

  * This buildpack expects that you have at least the heroku standard python buildpack. This buildpack should come first so that librdkafka gets installed before `pip install confluent-kafka` gets run.
  * Set up like so:
  ```
  heroku buildpacks:set https://github.com/MobileWorks/heroku-buildpack-librdkafka.git
  heroku buildpacks:add https://github.com/heroku/heroku-buildpack-python.git
  ```
