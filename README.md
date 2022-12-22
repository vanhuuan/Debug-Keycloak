# Debug-Keycloak

## I. Build Server Key-Cloak
- Required: Java version < 11; Mvn version 3.3+
- Checkout git repo: https://github.com/map4d/keycloak
- Cd keycloak
- Cmd: `mvn -Pdistribution -pl distribution/server-dist -am -Dmaven.test.skip clean install`
- Cmd: `tar xfz distribution/server-dist/target/keycloak-8.0.1.tar.gz`
- Cd keycloak-8.0.1
## II. Run build
- Cmd: `bin/standalone.[bat/sh]`
## III. Run debug
- Cmd : `bin/standalone.[bat/sh] -- debug xxxx`. xxxx: debug port number.
### Debug in intellij
- Open keycloak in Intelliji
- Chose configuration:
[image](https://user-images.githubusercontent.com/58378623/209035565-d4ace4d6-f271-46f1-a68a-64646613bbf5.png)
