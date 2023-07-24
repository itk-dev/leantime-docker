# Leantime docker setup for ITK

Docker hosting setup for Leantime. This merges our standard docker setup with
[docker-leantime](https://github.com/Leantime/docker-leantime)

See the leantime docs at https://docs.leantime.io for more info.

CLI commands defined by leantime can be run with docker compose, e.g:
```shell
docker compose exec leantime ./bin/leantime email:test --address=name@example.org
```

## Development

To run this setup locally for testing purposes, first create a `.env.local` file in the project root. Then up the containers.
```shell
touch .env.local
docker compose up -d
```

Then navigate to `<yourloacldomain>/install`and follow instructions to install database and set up first user account

## Production

Check out this repository on the server. Create a `.env.local` file in the project root and set the relevant values for database connection etc.

Then do `docker compose up -d`