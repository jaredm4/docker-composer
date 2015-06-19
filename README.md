# docker-composer

Simple Docker image to run Composer through Docker. This is mostly useful for Continuous Integration machines that support Docker, as a way to keep Composer out of your final production Docker application image.


## Usage
Simple Composer install in your current working directory's PHP app.

```
docker run --rm -v $(pwd):/project jaredm4/composer install -d /project
```

To enhance caching via sharing with the host.

```
docker run --rm -v $(pwd):/project -v $HOME/.composer:/root/.composer jaredm4/composer install -d /project
```

## License
[MIT](https://tldrlegal.com/license/mit-license)
