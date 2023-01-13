# Microservices


## Monolith

- Self contained application
- Entire application has to be re-deployed for a new feature

### Disadvantages
- Tight coupling (Inter-dependency of modules)
- Scaling is hard
- Teams must co-ordinate to develop any feature
- Restricted to the tech-stack

## Microservices
- Modular
- Independently Deployable
- Easy to scale
- Each microservice solves a single problem (Single functionality principle)
- Micro-services communicate via an interface
- Stateless, invocated asynchronously
- Fault Tolerant : Eliminates single point of failure
- Loose Coupling

### Disadvantages

- Difficult to define context boundary on a single micro-service
- Complex to setup load balancing to point to different micro-services

### Architecture
![image](https://user-images.githubusercontent.com/103091956/212238670-b537c450-f903-4598-bf80-25ae918cc8e5.png)
