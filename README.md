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

cf unbind-service APP_NAME SERVICE_INSTANCE
cf unbind-service moviefun albums-mysql

mvn clean package -DskipTests
cf push moviefun -p target/moviefun.war --random-route

git push -u other read-resource-from-classpath -f

git checkout -b write-to-blobstore write-to-blobstore-start
