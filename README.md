# FluentCI CI/CD demo for Ruby

This is an example application and CI/CD pipeline showing how to build, test a Ruby microservice using FluentCI.

Ingredients:

- Ruby Sinatra as web framework
- RSpec for tests

## Local application setup

To run the microservice:

```
fluentci run --wasm devbox run bundle config set path 'vendor/bundle'
fluentci run --wasm ruby bundle_exec rackup
```

To run tests:

```
fluentci run --wasm ruby bundle_exec rspec
```

To build and run Docker container:

```
docker build -t fluentci-demo-ruby .
docker run -p 80:4567 fluentci-demo-ruby
curl localhost
> hello world :))
```

## License

Distributed under the MIT License. See the file [LICENSE](./LICENSE).
