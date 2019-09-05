# The Movie DB Java API


[![](https://img.shields.io/badge/nextbss-opensource-blue.svg)](https://www.nextbss.co.ao)

Usage
---------------


### Download
To get a Git project into your build:


Step 1. Add the JitPack repository to your build file


maven
```xml
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>
```

gradle
```
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```


Step 2. Add the dependency


maven 
```xml
<dependency>
    <groupId>com.github.nextbss</groupId>
    <artifactId>tmdbv3-api</artifactId>
    <version>1.0</version>
</dependency>
```


gradle
```
dependencies {
    implementation 'com.github.nextbss:tmdbv3-api:1.0'
}
```


### Configuring api key
Set api key

Get an instance
```java
public class SomeClass{
    TmdbApi tmdbApi = TmdbApi.getInstance("API_KEY");
}
```

### get movie details
```java
public class SomeClass{
    TmdbApi tmdbApi = TmdbApi.getInstance("API_KEY");
    Movie movie = tmdbApi.movies().getDetailsRequestBuilder()
            .movieId(458156)
            .language(Languages.EN)
            .appendToResponse(AppendToResponse.ACCOUNT_STATES, AppendToResponse.ALTERNATIVE_TITLES)
            .send();
}
```

License
----------------


The library is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
