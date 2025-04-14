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

### Load Balancing
- Run the gateway api with cd gateway
- Then mvn spring-boot:run
- The load balancer will push traffic to either service a at http://localhost:8080/servicea/hello or to service b at http://localhost:8080/serviceb/hello. The service that does not receive traffic will have an empty page until the other service goes down, at which point that service will receive the traffic from then on.