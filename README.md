# Library Template using libGDX and Gradle 7.x

Change this to fit your library!

You'll want to edit gradle.properties to match your library's name, description, author, license, and so on.
You probably also want to edit build.gradle to match the projectName and group to what you want to use.

You should "Find in Files" and search for any places that use the word "template" in order to find anything
you will want to replace.

This version uses Gradle 7.6.2, which is probably the last 7.x release. It took a while, but Gradle 8.x is in
another branch of this repo and is much more stable now than it was at the start of 2023. Because Gradle 8.3
is fully compatible with Java 20 (Gradle 7.x is not), and people may try to compile with Java 20, you may want
to switch to the 8.x branch. If you have Gradle plugins that are only compatible with 7.x, though, feel free
to stay using this branch; it's been battle-tested and works fine.
