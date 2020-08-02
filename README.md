# README

So, you want a new Rails project but you don't want to fiddle around with managing Ruby versions, postgres, node, etc. Say no more! I'll make your life easier.

## Requirements

Docker and Docker Compose

## Setup

Just run `docker-compose up`, and on a separate terminal window, run `docker-compose run web bundle exec rails db:create`

## Migrations

In the future, when it's time run migrations, run `docker-compose run web bundle exec rails db:migrate`

## Notes

- Runs on Ruby 2.7.1 and Rails ~> 5.2.4
- This is only a copy of [Docker's quickstart guide](https://docs.docker.com/compose/rails/).