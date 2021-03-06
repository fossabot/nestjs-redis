# NestJS Redis
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FPokeGuys%2Fnestjs-redis.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FPokeGuys%2Fnestjs-redis?ref=badge_shield)


[ioredis](https://github.com/luin/ioredis) module for [Nest](https://github.com/nestjs/nest) that supported cluster, sentinel mode.

## Quick Start

### Installation

```bash
$ npm i --save @pg/nestjs-redis ioredis
# or
$ yarn add @pg/nestjs-redis ioredis
```

### Usage

```ts
// app.module.ts
@Module({
  imports: [
    RedisModule.forRoot({ uri: 'redis://localhost:6379/' }),
  ],
})
export class AppModule {}

// app.service.ts
@Injectable()
export class AppService {
  constructor(@InjectRedis() private readonly redis: RedisClient) {}
}
```

## Documentation

you can find all the documentation [here](docs/setup.md) for the redis module.

## License

[MIT License](LICENSE)


[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FPokeGuys%2Fnestjs-redis.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FPokeGuys%2Fnestjs-redis?ref=badge_large)