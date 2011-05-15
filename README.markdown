Jenkins/Phing for symfony 1.x
============================

This is a [**Phing**](http://phing.info/) `build.xml` for the [**symfony 1.x** framework](http://symfony-project.org/)
designed to be used with [**Hudson**](http://hudson-ci.org/)/[**Jenkins**](http://jenkins-ci.org/).

Usage
-----

* Copy the `build.xml` script in your project root directory.

* In Jenkins, add a **build step** like:

_Invoke Phing targets_:

> Targets: main

> Properties: projectName=MY_PROJECT_NAME

Or _Execute a shell script_:

    cd $WORKSPACE && phing main -DprojectName=$JOB_NAME

* Now, you can customize each _fileset_ to fit your needs :-)

Warning
-------

To use the `phploc` target, you have to install the [**PHPLoc Phing task**](https://github.com/raphaelstolt/phploc-phing).
Just copy the `PHPLocTask.php` file somewhere like `/usr/share/php/phing/tasks/my/` (create the `my` directory if needed).

TIPS
----

I recommand you to use the amazing phpDocumentor theme [JEvolve](http://themouette.github.com/JEvolve/).

To use it, just change the `ouput` parameter of the `phpdoc` task like the code below:

    output="HTML:Smarty/JEvolve:default"


William.
