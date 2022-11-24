Spring Dependencies:

https://start.spring.io/#!type=maven-project&language=java&platformVersion=2.7.5&packaging=jar&jvmVersion=19&groupId=com.stefan&artifactId=user-service&name=user-service&description=User%20service&packageName=com.stefan.user-service&dependencies=native,lombok,web,validation,prometheus,actuator,webflux,amqp,mysql,data-jpa

Spring 3.0.0-SNAPSHOT:

https://start.spring.io/#!type=maven-project&language=java&platformVersion=3.0.0-SNAPSHOT&packaging=jar&jvmVersion=19&groupId=com.stefan&artifactId=user-service&name=user-service&description=User%20service&packageName=com.stefan.user-service&dependencies=native,lombok,web,validation,cloud-starter-zipkin,cloud-starter-sleuth,prometheus,actuator,webflux,amqp,mysql,data-jpa

$ ./mvnw -PnativeTest test
./mvnw -PnativeTest package 

-----------------------------------------------
                       Run

./mvnw -Pnative -DskipTests clean package --enable-preview 

sdk use java graalVM-19

native-image -jar target/user-service-0.0.1-SNAPSHOT.jar --static --libc=musl -o target/user-app
