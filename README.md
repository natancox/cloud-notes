# cloud-notes

## Consul

Summary from good presentation https://www.youtube.com/watch?v=cJUTIyvCd70 

Multiple functions

1) service registration
- can do DNS
- health checks (activator boot!)
- can register "anything" (DB nodes...)

Ribbon integration
- client-side load balancer
- health check on ribbon (not supported by Eureka!)

2) K/V store
- for configuration
- path => convert to "blob" (json)
====================> TODO : check model !!

3) Events

consul-starter-bus => spring cloud stream impl (abstraction of Kafka/Consul/...)

4) ACL

Hide services / configuration through security !


Code

1) setup
@EnableDiscoveryClient
bootstrap.properties => used before app "boots"

2) configs are "hierarchical"
- generic application properties
- generic profile properties
- app specific application properites
- app specific profile properties

