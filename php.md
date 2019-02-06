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

