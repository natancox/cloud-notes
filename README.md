# cloud-notes

## Consul

Summary from good presentation https://www.youtube.com/watch?v=cJUTIyvCd70. Watch it at speed 1.5.

  1. Make my changes
    1. Fix bug
    2. Improve formatting
      * Make the headings bigger
  2. Push my commits to GitHub
  3. Open a pull request
    * Describe my changes
    * Mention all the members of my team
      * Ask for feedback

### Multiple functions

1. Service registration
  1. can do DNS
  2. health checks 
    * enable activator boot to view info
  3. can register "anything", not only services (like DB nodes...)
  4. ribbon integration
    * is a client-side load balancer
    * health check on ribbon (not supported by Eureka!)
2. K/V store
  * for configuration
  * path => convert to "blob" (json?)

> TODO : check model !!

3. Events
  * consul-starter-bus is a spring cloud stream implemenation (like Kafka)
4. ACL
  * security
  * possible to hide services / configuration


### Code

1. setup

Add annotation

```
@EnableDiscoveryClient
```

Rename `application.properties` to `bootstrap.properties`. Uses 'boot' step before application really starts.

2) configs are "hierarchical"
- generic application properties
- generic profile properties
- app specific application properites
- app specific profile properties

