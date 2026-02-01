# Library Template using libGDX and Gradle 9.x

Change this to fit your library!

Normally you use this repo by forking it, making any changes to match future projects you will want to make,
and then using this repo as a template when you make a new project. This often involves changing the packages
from `com.github.tommyettinger` to your own reverse domain name or to use your own GitHub username.

You'll want to edit gradle.properties to match your library's name, description, author, license, and so on.
You probably also want to edit build.gradle to match the projectName and group to what you want to use.

You should "Find in Files" and search for any places that use the word "template" in order to find anything
you will want to replace. The search should be case-insensitive.

This includes some extra configuration so that you can deploy more easily to [JitPack](https://jitpack.io). If you're
testing a specific commit and don't want to push a release to GitHub or Maven Central just to test (especially
if testing by seeing if a user can build with your library), then JitPack is a great option. It can also be an
excellent way of making GitHub releases available via Maven or Gradle dependencies. The `jitpack.yml` file this
includes defaults to Java 21; you can potentially raise this as high as 25, though that might cause problems
with Kotlin or libraries like Kryo, or as low as 11 (the minimum for the publishing plugin this uses). JDK 21
may warn if you target Java 8, though this is only a warning. It has better generated JavaDocs than earlier
versions, though, so using 21 seems good.

Regardless of which JDK version JitPack uses to build, the default sourceCompatibility, targetCompatibility, and
release are set to JDK 8, which supports many of the most convenient recent Java features, but not all. You can
increase those to a higher version to get features like `var`, records, pattern matching, etc. but that typically
will limit your library to being used by desktop builds (LWJGL 2 or 3, server, or headless). Using the language
level of Java 8 is generally safe, but specific APIs added in Java 8 generally aren't available in RoboVM, GWT,
or some versions of Android. You can go up to compatibility with 11 to get access to `var`, but then you lose
all compatibility with RoboVM.

The test code, which goes in `src/test/java/`, uses compatibility with Java 8 by default, so you can use LWJGL3
in tests out-of-the-box.

This currently uses Gradle 9.x; if you want an earlier version that uses 8.x,
[here you go for 8](https://github.com/tommyettinger/libgdx-library-template/releases/tag/v8.14.3)!
If you still want the much-earlier version that uses Gradle 7,
[here you go for 7](https://github.com/tommyettinger/libgdx-library-template/releases/tag/v7.6)!
