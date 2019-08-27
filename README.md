# Packagist Mirror

This is a project for creating a mirror site of Packagist, PHP package repository.

If you're using Composer, commands like `create-project`, `require`, `update`, 
`remove` are often used. When those commands are executed, Composer downloads 
the JSON file containing the package information from Packagist, and downloads 
the necessary packages and the JSON files of the packages that depend on them. 
Depending on the complexity of the package, you can download dozens or hundreds 
of JSON files. The further you are from the location of the Packagist server, 
the more time is needed to download those JSON files. By using mirror, it will 
help save the time for downloading because the server location is closer.

This project aims to create a local mirror with ease, allowing greater 
availability for companies that want to use the Composer but do not want to 
depend on the infrastructure of third parties. It is also possible to create 
a public mirror to reduce the load on the main repository and allow a better 
distribution of requests around the world.

## Install

Via Composer

``` bash
$ git clone https://github.com/Webysther/packagist-mirror.git
$ cd packagist-mirror && composer install
$ cp .env.example .env # and modify .env file
```

Schedule the command to create and update the mirror:

```bash
$ php bin/mirror create --no-progress
```

Via Docker

Follow to [docker repository](https://github.com/Webysther/packagist-mirror-docker).

## Requirements

The following versions of PHP are supported by this version.

* PHP >= 7.1

## Testing

``` bash
$ vendor/bin/phpunit
```

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) and [CONDUCT](CONDUCT.md) for details.

## Credits

- [Ian Mustafa](https://github.com/ianmustafa)
- [Webysther Nunes](https://github.com/Webysther)
- [Hiraku NAKANO](https://github.com/hirak)
- [IndraGunawan](https://github.com/IndraGunawan)
- [All Contributors](https://github.com/Webysther/packagist-mirror/contributors)

## License

MIT License. Please see [License File](LICENSE) for more information.
