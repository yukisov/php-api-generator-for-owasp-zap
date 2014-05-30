php-api-generator-for-owasp-zap
===============================

PHP client API generator for OWASP ZAP

##Getting Started

1. Preparing zaproxy project in your local environment.
    - We assume to use [Eclipse](http://www.eclipse.org/) in this 'Getting Started.
    - Ref. [Building - zaproxy](https://code.google.com/p/zaproxy/wiki/Building)
2. Copy & paste PhpAPIGenerator.java to zaproxy project `src` directory.
    - `$ cp ./src/org/zaproxy/zap/extensions/api/PhpAPIGenerator.java your/zaproxy/src/org/zaproxy/zap/extensions/api/`
3. Copy & paste Zapv2.php to zaproxy project `php/api/src/Zap` directory.
    - `$ mkdir -p your/zaproxy/php/api/src/Zap`
    - `$ cp php/api/src/Zap/Zapv2.php your/zaproxy/php/api/src/Zap/`
3. Patch build.xml
    1. `$ cp ./build.xml.patch your/zaproxy/build/`
    2. `$ cd your/zaproxy/build`
    3. `$ patch build.xml < build.xml.patch`
4. Right click zaproxy project and select 'Refresh'.
5. Right click zaproxy project and select 'Build Project'.
6. Create PHP client API files.
    - `$ cd your/zaproxy/build`
    - `$ ant generate-apis`
        - This process needs `your/zaproxy/bin/org/src/zaproxy/zap/extension/api/PhpAPIGenerator.class` file.
7. PHP client API files are created in `your/zaproxy/php/api/src/Zap/`


##License
- MIT License