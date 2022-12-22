# Debug-Keycloak

## I. Build Server Key-Cloak
- Required: Java version < 11; Mvn version 3.3+
- Checkout git repo: https://github.com/map4d/keycloak
- Cd keycloak
- Cmd: `mvn -Pdistribution -pl distribution/server-dist -am -Dmaven.test.skip clean install`
- Cmd: `tar xfz distribution/server-dist/target/keycloak-8.0.1.tar.gz`
- Cd keycloak-8.0.1
- Add 3 jars file in to folder: `keycloak-8.0.1\modules\system\layers\keycloak\org\keycloak\keycloak-services\main`

![image](https://user-images.githubusercontent.com/58378623/209045465-954a28f3-3cce-42a0-9cbb-028a8dd33448.png)

- Add folder `postgresql` in git repo to: `keycloak-8.0.1\modules\system\layers\keycloak\org`
## II. Run build
- Cmd: `bin/standalone.[bat/sh]`
## III. Run debug
- Cmd : `bin/standalone.[bat/sh] -- debug xxxx`. xxxx: debug port number.
### Debug in intellij
+ Open keycloak project in Intelliji:
+ Chose configuration:

![image](https://user-images.githubusercontent.com/58378623/209035565-d4ace4d6-f271-46f1-a68a-64646613bbf5.png)

+ Click Add New Configuration:

![image](https://user-images.githubusercontent.com/58378623/209036059-e0d9f87d-8c0c-416e-9346-4f2429e2c0df.png)

+ Select Remote JVM Debug:

![image](https://user-images.githubusercontent.com/58378623/209036251-d16c275f-f167-4d26-aee7-07669b14b5bb.png)

+ Config setting ( Host: Server ip, port: debug port number )

![image](https://user-images.githubusercontent.com/58378623/209036387-35427bf9-33b3-4d4a-a634-38c64dc08bbf.png)

+ Then click Apply and Save.
+ To run debug, select debugger and click debug button: 

![image](https://user-images.githubusercontent.com/58378623/209036760-f23e7dbd-da57-4605-b201-72c8e921830b.png)

+ Click Stop button to stop debug, we can start debug again without restart server:

![image](https://user-images.githubusercontent.com/58378623/209036923-a2078b5a-2662-48c8-8902-ffa1d7272c86.png)

### Debug in Eclipse

+ Open keycloak project in Eclipse:

+ Go to Run -> Debug Configurations:

![image](https://user-images.githubusercontent.com/58378623/209044611-28f24036-7aa9-429f-b94c-7ba0dcb1c3cd.png)

+ Create a new Remote Java Application configuration:

![image](https://user-images.githubusercontent.com/58378623/209044662-af48692a-a64b-42b0-9d73-0f0024ea0556.png)

+ Configure the remote application's details

![image](https://user-images.githubusercontent.com/58378623/209044719-13a36132-0a4a-4ad8-bbef-bf90df0e3564.png)

+ Click debug button to start debug:

![image](https://user-images.githubusercontent.com/58378623/209044808-5d63dcc3-e94b-424f-8d17-3f45187692d4.png)

+ Click Run -> Disconnect to stop debug:

![image](https://user-images.githubusercontent.com/58378623/209045158-1a588f2d-af03-4d77-a58e-c4f9ddda1233.png)


