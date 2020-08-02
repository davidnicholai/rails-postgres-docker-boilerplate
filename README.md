# README

So, you want a new Rails project but you don't want to fiddle around with managing Ruby versions, postgres, node, etc. Say no more! I'll make your life easier.

## Requirements

Docker and Docker Compose

## Setup

- Just run `docker-compose up`, and on a separate terminal window, run `docker-compose run web bundle exec rails db:create`
- Your Rails app is on [http://localhost:3000](http://localhost:3000)

## Tips

- To generate controllers and the like, run `docker-compose run web bundle exec rails g controller Foo`
- The above command will generate files, however it'll be owned by root (if you check via `ls -la`) to fix this, run `sudo chown -R $USER:$USER .`

## Migrations

In the future, when it's time run migrations, run `docker-compose run web bundle exec rails db:migrate`

## Notes

- Runs on Ruby 2.7.1 and Rails ~> 5.2.4
- This is only a copy of [Docker's quickstart guide](https://docs.docker.com/compose/rails/).
