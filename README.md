## Gradle build failure example

Running `gradle test` will fail in this example,
even though it _appears_ as though build.gradle ignores SystemTests during the `test` phase.

Moving the `apply plugin: groovy` inside of `allprojects` will cause it to succeed,
because the failing test will be ignored because the configuration will be passed to
subprojects.

Based on [a tweet](https://twitter.com/matthew_dailey1/status/867746998849589250) of mine.

## Reproducibility

```
matt@MacBook-Pro-6 (master) gradle-quirks$ ../some-other-repo/gradlew --version

------------------------------------------------------------
Gradle 3.5
------------------------------------------------------------

Build time:   2017-04-10 13:37:25 UTC
Revision:     b762622a185d59ce0cfc9cbc6ab5dd22469e18a6

Groovy:       2.4.10
Ant:          Apache Ant(TM) version 1.9.6 compiled on June 29 2015
JVM:          1.7.0_80 (Oracle Corporation 24.80-b11)
OS:           Mac OS X 10.11.6 x86_64
```

## License

MIT License
