# PHP

## Composer

### Adding source directories

In the `composer.json` file add the `autoload` field.

For example:

<pre>
  "autoload": {
        "psr-4": {"hdvianna\\": "src/"}
   }
</pre>

Then, run `composer` with `dump-autoload` to regenerate the autoload file.
For example:
<pre>
>composer dump-autoload
</pre>

### Creating project 

```bash
composer create project --prefer-dist <package> <project-name> 
```

Example

```bash
composer create project --prefer-dist laravel/laravel blog 
```

## Symfony

### Api docs

Apis docs can be found at https://api.symfony.com/4.2/index.html

### Symfony client

Symfony client is available for download at https://symfony.com/download

#### Creating a new full symfony project 
<pre>
>symfony new &lt;project_name&gt;
</pre>

#### Serving the project
<pre>
>symfony serve
</pre>

## php.ini

### Allowing short open tags

Allowing the use of `<?` for opening php scripts

<pre>
short_open_tag=On
</pre>

### Other configurations

`post_max_size`

`upload_max_filesize`

`memory_limit`

## Resources

### Awesome PHP

"Awesome PHP" is a list with plenty of PHP helpful links: https://github.com/ziadoz/awesome-php
