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

cf push moviefun -p target/moviefun.war --random-route

mkdir -p ~/shared/moviefun

minio server ~/shared

export VCAP_SERVICES='{"user-provided": [{"credentials": {"access_key_id": "AAAAAAAAA", "bucket": "moviefun", "secret_access_key": "SSSSSSSSS", "endpoint": "http://127.0.0.1:9000"}, "name": "photo-storage"}]}'
export VCAP_SERVICES='{"user-provided": [{"credentials": {"access_key_id": "L4R6NX1RC8W1JGH4CYJI", "bucket": "moviefun", "secret_access_key": "k26TWpk77YdruftNyCDtENUuA7E3jGay0GfEOHLp", "endpoint": "http://127.0.0.1:9000"}, "name": "photo-storage"}]}'

mvn spring-boot:run

cf push moviefun --random-route --no-start -p target/moviefun.war

cf create-user-provided-service SERVICE_INSTANCE [-p CREDENTIALS] [-l SYSLOG_DRAIN_URL] [-r ROUTE_SERVICE_URL] [-t TAGS]
cf cups SERVICE_INSTANCE [-p CREDENTIALS] [-l SYSLOG_DRAIN_URL] [-r ROUTE_SERVICE_URL] [-t TAGS]

Linux/Mac:
cf cups my-db-mine -p '{"username":"admin","password":"pa55woRD"}'

cf cups photo-storage -p '{"access_key_id":"AKIAJQTUFHPLLNDIBCWQ","secret_access_key":"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","bucket":"student-artifacts-newyork"}'
cf delete-service photo-storage

cf bind-service APP_NAME SERVICE_INSTANCE [-c PARAMETERS_AS_JSON] [--binding-name BINDING_NAME]
cf bind-service moviefun photo-storage

cf unbind-service APP_NAME SERVICE_INSTANCE
cf unbind-service moviefun photo-storage

cf start APP_NAME
cf start moviefun