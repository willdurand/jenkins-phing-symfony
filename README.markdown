Hudson/Phing for symfony 1.x
============================

This is a [**Phing**](http://phing.info/) `build.xml` for the [**symfony 1.x** framework](http://symfony-project.org/)
designed to be used with [**Hudson**](http://hudson-ci.org/)/[**Jenkins**](http://jenkins-ci.org/).

Usage
-----

* Copy the `build.xml` script in your project root directory.

* In Hudson, add a **build step** like:

_Invoke Phing targets_:

> Targets: main

> Properties: projectName=MY_PROJECT_NAME

Or _Execute a shell script_:

    cd $WORKSPACE && phing main -DprojectName=$JOB_NAME

* Now, you can customize each _fileset_ to fit your needs :-)


William.
