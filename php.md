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
