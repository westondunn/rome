# ROME

[![Build Status](https://travis-ci.org/rometools/rome.svg?branch=master)](https://travis-ci.org/rometools/rome)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.rometools/rome/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.rometools/rome)

ROME is a Java framework for RSS and Atom feeds. The framework consist of several modules:

| Module | Description |
| ------ | ----------- |
| `rome` | Library for generating and parsing RSS and Atom feeds. |
| `rome-modules` | Generators and parsers for extensions like MediaRSS, GeoRSS and others. |
| `rome-opml` | [OPML](https://en.wikipedia.org/wiki/OPML) parsers and tools. |

Deprecated modules: `rome-fetcher`, `rome-certiorem`, `rome-certiorem-webapp` and `rome-propono`.

## Changelog

### 1.6.0

- [Upgrade of JDOM to version 2.0.5](https://github.com/rometools/rome/issues/197)
- [Maven plugin and dependency updates](https://github.com/rometools/rome/issues/268)
- [Support for allowing Doctype declarations in rome-fetcher](https://github.com/rometools/rome/issues/234)
- [OSGi improvements](https://github.com/rometools/rome/issues/143) 

### 1.5.1

- solved an [XML bomb](https://en.wikipedia.org/wiki/Billion_laughs) vulnerability

Important note: due to the security fix ROME now forbids all Doctype declarations by default. This will break compatibility with RSS 0.91 Netscape
because it requires a Doctype declaration. When you experience problems you have to activate the property **allowDoctypes** on the SyndFeedInput object. You 
should only use this possibility when the feeds that you process are absolutely trustful.

### 1.5.0

- many (untracked) enhancements
- code cleanup
- renamed packages (was required to be able to push to Maven Central after years again)
- updated sourcecode to Java 1.6

### Prior to 1.5.0

- see [http://rometools.github.io/rome/ROMEReleases](http://rometools.github.io/rome/ROMEReleases) 
