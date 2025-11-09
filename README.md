# CodeNarc IntelliJ Plugin

## Version 7.0.0

New features:
- Compatible with IntelliJ IDEA 2025.2+ (based on IntelliJ Plugins v2)
- Supports [Disabling rules from comments](https://codenarc.org/codenarc-configuring-rules.html#disabling-rules-from-comments)
- Gradle 9.2.0
- CodeNarc 3.6.0
- Groovy 4+
- Default run configuration for debugging the plugin in IDEA

Regression:
- Existing Quick Fixes are not compatible with the new IDEA QuickFix API, so they were removed

## Development

To run the plugin locally run `./gradlew runIde`

## Build

To build the plugin run `./gradlew build -x test`.
Take the file from `build/distributions/codenarc-idea-7.0.0-SNAPSHOT.zip` and install it in IDEA.

## Beta Channel
Feel free to join the beta channel here: https://plugins.jetbrains.com/plugins/beta/5925

![add custom repositories](static/images/add-repository-1.png)

![add custom repository](static/images/add-repository-2.png)

## Known Issues

There is [a random issue with `StackOverflowError`](https://github.com/melix/codenarc-idea/issues/45) which should have no impact on the IDE. 

## History

This is an update to this project:

https://github.com/seanleblanc/CodeNarc-Updated

which was an update to this project:

https://github.com/melix/CodenarcNG

which was a fork the original project.

CodeNarc-Updated will be replaced with this plugin.

## Upgrading CodeNarc

1. Change the version in `build.gradle`
2. Run `./gradlew run` to regenerate the inspection classes (existing inspection classes manual removal from 
   `org.codenarc.idea.inspections` might be required)
3. Run `./gradlew build -x test`
4. Take the file from `build/distributions/codenarc-idea-7.0.0-SNAPSHOT.zip` and install it in IDEA.



