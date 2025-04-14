# MSA-Case-Study

## How to run

### Server
- cd eureka-server <br>
- mvn spring-boot:run
- Navigate to http://localhost:8761/

### Client
- cd servicea or cd serviceb <br>
- mvn spring-boot:run
- To ensure it is working, navigate to http://localhost:8081/hello for service a, and http://localhost:8082/hello for service b.

Run both at the same time. The more clients added, the more you will see appear under the instances tab in the eureka-server