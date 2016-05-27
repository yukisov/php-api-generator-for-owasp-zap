php-api-generator-for-owasp-zap
===============================

PHP client API generator for OWASP ZAP

## Generating PHP client API files

1. Preparing the zaproxy repository in your local environment.
    - Git clone a repository from [zaproxy/zaproxy: The OWASP ZAP core project](https://github.com/zaproxy/zaproxy).
    - Ref. [Building · zaproxy/zaproxy Wiki](https://github.com/zaproxy/zaproxy/wiki/Building)
2. Copy & paste PhpAPIGenerator.java to zaproxy project `src` directory.

	```
    $ cp ./src/org/zaproxy/zap/extensions/api/PhpAPIGenerator.java your/zaproxy/src/org/zaproxy/zap/extensions/api/
    ```

3. Copy & paste Zapv2.php to zaproxy project `php/api/src/Zap` directory.

	```
    $ mkdir -p your/zaproxy/php/api/src/Zap
    $ cp php/api/src/Zap/Zapv2.php your/zaproxy/php/api/src/Zap/
    ```

4. Right click zaproxy project and select 'Refresh' (in Eclipse).
5. Right click zaproxy project and select 'Build Project' (in Eclipse).
6. Create PHP client API files.

	```
    $ cd your/zaproxy/build
    $ ant generate-apis
    ```

    This process needs `your/zaproxy/bin/org/src/zaproxy/zap/extension/api/PhpAPIGenerator.class` file.

7. PHP client API files have been created in `your/zaproxy/php/api/src/Zap/`


## License

- Apache License, Version 2.0
