# Movie Fun!

Smoke Tests require server running on port 8080 by default.

## Build WAR ignoring Smoke Tests

```
$ mvn clean package -DskipTests -Dmaven.test.skip=true
```

## Run Smoke Tests against specific URL

```
$ MOVIE_FUN_URL=http://moviefun.example.com mvn test
```
git checkout -b write-to-blobstore write-to-blobstore-start
git commit -am "CsvUtils.java"

mvn clean package -DskipTests
mvn spring-boot:run