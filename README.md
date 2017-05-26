## Gradle build failure example

Running `gradle test` will fail in this example,
even though it _appears_ as though build.gradle ignores SystemTests during the `test` phase.

Moving the `apply plugin: groovy` inside of `allprojects` will cause it to succeed,
because the failing test will be ignored because the configuration will be passed to
subprojects.

Based on [a tweet](https://twitter.com/matthew_dailey1/status/867746998849589250) of mine.

## License

MIT License
