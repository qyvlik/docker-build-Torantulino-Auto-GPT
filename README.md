# docker-build-yairm210-unciv

Auto build https://github.com/qyvlik/Auto-GPT, See https://hub.docker.com/r/qyvlik/autogpt

## docker-compose

```bash
# To boot the app run the following:
# docker-compose run auto-gpt
version: "3.9"

services:
  autogpt:
    image: qyvlik/autogpt:develop
    command: --debug --gpt3only
    volumes:
      - ".env:/app/.env"
    profiles: ["exclude-from-up"]

  redis:
    image: "redis/redis-stack-server:latest"
```

- .env file See https://github.com/qyvlik/Auto-GPT/blob/develop/.env.template
