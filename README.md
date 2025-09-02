[maven-central]: https://img.shields.io/maven-central/v/net.dv8tion/JDA?filter=!*-preview*&logo=apachemaven&color=blue
[jitpack]: https://img.shields.io/badge/Snapshots-JitPack?logo=jitpack
[installation]: #-installation
[discord-invite]: https://discord.gg/0hMr4ce0tIl3SLv5
[license]: https://github.com/discord-jda/JDA/tree/master/LICENSE
[faq]: https://jda.wiki/introduction/faq/
[docs]: https://docs.jda.wiki/index.html
[wiki]: https://jda.wiki/introduction/jda/
[troubleshooting]: https://jda.wiki/using-jda/troubleshooting/
[discord-shield]: https://discord.com/api/guilds/125227483518861312/widget.png
[faq-shield]: https://img.shields.io/badge/Wiki-FAQ-blue.svg
[docs-shield]: https://img.shields.io/badge/Wiki-Docs-blue.svg
[troubleshooting-shield]: https://img.shields.io/badge/Wiki-Troubleshooting-darkgreen.svg
[license-shield]: https://img.shields.io/badge/License-Apache%202.0-white.svg
[GatewayIntent]: https://docs.jda.wiki/net/dv8tion/jda/api/requests/GatewayIntent.html
[JDABuilder]: https://docs.jda.wiki/net/dv8tion/jda/api/JDABuilder.html
[DefaultShardManagerBuilder]: https://docs.jda.wiki/net/dv8tion/jda/api/sharding/DefaultShardManagerBuilder.html

<img align="right" src="https://github.com/discord-jda/JDA/blob/assets/assets/readme/logo.png?raw=true" height="150" width="150">

[![maven-central][]][installation]
[![jitpack][]](https://jitpack.io/#discord-jda/JDA)
[![license-shield][]][license]

[![discord-shield][]][discord-invite]
[![faq-shield]][faq]
[![docs-shield]][docs]
[![troubleshooting-shield]][troubleshooting]

# JDA (Java Discord API)

This is a fork of the Java Discord wrapper, JDA, which includes a couple extra goodies:

1. The new Discord Label and Select components are able to be used in Modal's (see discord-jda/JDA#2162)
2. Bots can appear as on mobile. See below:

```kt
val jda = JDABuilder.createDefault(token)
  .withMobileIdentify()
```

This works by changing the identify packet (sent first in Gateway) to `Discord iOS`, making the bot appear on mobile.

Thats it! Apart from that, this fork is exactly the same.

## Maven

```xml
<repositories>
  <repository>
    <id>jitpack.io</id>
	<url>https://www.jitpack.io</url>
  </repository>
</repositories>
<dependency>
  <groupId>com.github.giftedl</groupId>
  <artifactId>JDA</artifactId>
  <version>-11d8917c26-1</version>
</dependency>
```

## Kotlin Gradle

```kts
dependencyResolutionManagement {
  repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
  repositories {
    mavenCentral()
    maven { url = uri("https://www.jitpack.io") }
  }
}

dependencies {
  implementation("com.github.giftedl:JDA:-11d8917c26-1")
}
```

## Groovy Gradle

```
dependencyResolutionManagement {
  repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
  repositories {
    mavenCentral()
	maven { url 'https://www.jitpack.io' }
   }
}

dependencies {
  implementation 'com.github.giftedl:JDA:-11d8917c26-1'
}
```
