# cloud-notes

## Consul

Summary from good presentation https://www.youtube.com/watch?v=cJUTIyvCd70. Watch it at speed 1.5.

### Multiple functions

1. Service registration
  * can do DNS
  * health checks 
    * enable activator boot to view info
  * can register "anything", not only services (like DB nodes...)
  * ribbon integration
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

2. Important: configs are "hierarchical"

- generic application properties
- generic profile properties
- app specific application properties
- app specific profile properties

More specific properties have priority over less specific ones.

## Vault

Summary from good presentation starting at 39.45 on https://www.youtube.com/watch?v=cJUTIyvCd70. Watch it at speed 1.5.

Vault is a tool from Hashicorp to manage secrets.

* secure secret storage
* audit logs
* dynamic secrets (expiration)
* leasing and renewal
* revocation (one node or a full tree)
* encryption as a service

Very simple API for secrets
* read
* write

Storage does not really matter.

Demo of : vault - consul integration

