# PHP

## Composer

### Adding source directories

In the `composer.json` file add the `autoload` field.

For example:

```json
  "autoload": {
        "psr-4": {"hdvianna\\": "src/"}
   }
```

Then, run `composer` with `dump-autoload` to regenerate the autoload file.
For example:
```bash
composer dump-autoload
```

### Creating project 

```bash
composer create project --prefer-dist <package> <project-name> 
composer create-project  <package> <project-name> 
```

Examples

```bash
composer create project --prefer-dist laravel/laravel blog 

composer create-project symfony/website-skeleton demo
```

## Symfony

### Api docs

Apis docs can be found at https://api.symfony.com/4.2/index.html

### Symfony client

Symfony client is available for download at https://symfony.com/download

#### Creating a new full symfony project 
```bash
symfony new <project-name>
```

#### Serving the project
```bash
symfony serve
```

## php.ini

### Allowing short open tags

Allowing the use of `<?` for opening php scripts

```ini
short_open_tag=On
```

### Other configurations

`post_max_size`

`upload_max_filesize`

`memory_limit`

## Resources

### Awesome PHP

"Awesome PHP" is a list with plenty of PHP helpful links: https://github.com/ziadoz/awesome-php
