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

## Symfony

### Symfony client

Symfony client is available for download at https://symfony.com/download

#### Create a new full symfony project 
<pre>
>symfony new <project_nama>
</pre>

#### Serving the project
<pre>
>symfony serve
</pre>


