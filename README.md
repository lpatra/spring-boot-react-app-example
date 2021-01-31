# Introduction

This is an example project to show integration of a rect app within a spring boot app.

# How it was done?
- Under the root folder the react app was created using [create-react-app](https://create-react-app.dev/)
- Under the root folder the spring boot app was created using [spring initializer](https://start.spring.io/)
- By creating the following symlink the react app contents became static assets of the spring boot app
```bash
cd spring-boot-app/src/main/resources
ln -s ../../../../react-app/build static
```

# How to build and run?
- Before building the spring boot app, one needs to build the react app. Use the following command from the root folder to build
```bash
cd react-app && npm run build && cd - && cd spring-boot-app && gradle build && cd -;
```
- Then you can run the spring boot application jar as follows
```bash
java -jar spring-boot-app/build/libs/spring-boot-app-0.0.1-SNAPSHOT.jar
```
