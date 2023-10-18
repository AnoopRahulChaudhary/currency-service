# currency-service
This is Microservice-Demo project.

This service comprised of following microservices -
1. currency conversion service - https://github.com/AnoopRahulChaudhary/currency-conversion-service
2. currency exchange service - https://github.com/AnoopRahulChaudhary/currency-exchange-service
3. api gateway - https://github.com/AnoopRahulChaudhary/api-gateway
4. naming service (Service Discovery) - https://github.com/AnoopRahulChaudhary/naming-service
5. using zipkin server to trace the api-request.

How to start the service -
- Required software - git, docker
- Run following command after making sure that you have installed git and docker in the system. 
1. clone the project - `git clone https://github.com/AnoopRahulChaudhary/currency-service.git`
2. Go inside the `currency-service` project by running command `cd currency-service/`.
3. Run the command `docker compose up`

Check if all services up, for following health urls, we should get `UP` service status -
currency-exchange : http://localhost:8000/actuator/health
currency-conversion : http://localhost:8100/actuator/health
api-gateway: http://localhost:8765/actuator/health
naming service: http://localhost:8761/actuator/health
zipkin server: http://localhost:9411/actuator/health


When all server are up after `docker compose up` command we can test following api -
via api-gateway -
 - http://localhost:8765/currency-exchange/from/USD/to/INR
 - http://localhost:8765/currency-conversion/from/USD/to/INR/quantity/10

Zipkin url to trace the request - http://localhost:9411/zipkin/
