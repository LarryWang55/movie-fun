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

git remote add origin https://github.com/LarryWang55/movie-fun.git

git push -u origin master --tags

mvn clean package -DskipTests -Dmaven.test.skip=true

export TOMEE_DIRECTORY=/home/pal_user/dev/tomee

cp target/moviefun.war /home/pal_user/dev/tomee/webapps

/home/pal_user/dev/tomee/bin/catalina.sh run

open http://localhost:8080/moviefun

MOVIE_FUN_URL=https://moviefun-zany-parrot.apps.pikes.pal.pivotal.io mvn test

cf push moviefun -p target/moviefun.war -b https://github.com/cloudfoundry-community/tomee-buildpack.git --random-route

cf create-service SERVICE PLAN SERVICE_INSTANCE [-c PARAMETERS_AS_JSON] [-t TAGS]
cf create-service p-mysql 100mb movies-mysql

cf bind-service moviefun movies-mysql
cf restage moviefun

-------------------------------------------------
curl https://spring-cloud-broker.apps.pikes.pal.pivotal.io/info
"version":"1.5.2-build.9"

-------------------------------------------------
mvn spring-boot:run

cf push moviefun -p target/moviefun.war -b ${JAVA_BUILDPACK_NAME} --random-route
cf push moviefun -p target/moviefun.war -b java_buildpack_offline --random-route
cd ~/workspace/assignment-submission
./gradlew replatformingSpringBootification -PmovieFunUrl=https://moviefun-zany-parrot.apps.pikes.pal.pivotal.io

