[![](https://badge.imagelayers.io/brtnshrdr/sbt:latest.svg)](https://imagelayers.io/?images=brtnshrdr/sbt:latest 'Get your own badge on imagelayers.io')

# What is SBT?

![logo](https://raw.githubusercontent.com/1science/docker-sbt/latest/logo.png)

sbt is an open source build tool for Scala and Java projects, similar to Java's Maven or Ant.

> [wikipedia.org/wiki/SBT_(software))

This image is based on OpenJDK 8.


# Supported tags

-	[`0.13.15-openjdk-8`](https://github.com/brtnshrdr/docker-sbt/tree/0.13.15-oracle-jdk-8)


# Usage

You can run the default `sbt` command simply:

```
 docker run -ti --rm 1science/sbt sbt sbt-version 
```

This image is configured with a workdir `/app`, so to build your project you have to mount a volume for your sources and another at `/root/.ivy2` to hold the ivy cache artifacts :

```
docker run -ti --rm -v "$PWD:/src" -v "$HOME/.ivy2":/root/.ivy2 1science/sbt sbt clean compile
```


# License

All the code contained in this repository, unless explicitly stated, is
licensed under ISC license.

A copy of the license can be found inside the [LICENSE](LICENSE) file.
