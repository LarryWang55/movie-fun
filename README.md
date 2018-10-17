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


mvn clean package -DskipTests -Dmaven.test.skip=true

cf push moviefun -p target/moviefun.war --random-route

cf create-service SERVICE PLAN SERVICE_INSTANCE [-c PARAMETERS_AS_JSON] [-t TAGS]
cf create-service p-mysql 100mb albums-mysql

cf bind-service APP_NAME SERVICE_INSTANCE [-c PARAMETERS_AS_JSON] [--binding-name BINDING_NAME]
cf bind-service moviefun albums-mysql

git checkout -b two-data-sources

git commit -am "work in progress"

git push -u other two-data-sources -f
