# Vertical scalability
Vertical scalability is only a good option for small applications. One of the main trade-offs is that it promotes monolithic architectures, which can require significant effort to overcome as horizontal scalability becomes more attractive.

Secondly, operating system and application design may limit the ability to effectively utilize a powerful single machine. For example, a database may struggle to use a very large number of cores due to lock contention issues. Effective lock management is complex, and it is often difficult to manage high levels of concurrency.

# Horizontal scalability
In the real world, true horizontal scaling for all services is difficult and expensive. Systems should start by scaling horizontally in key areas like web servers and caches before tackling more difficult areas like persistent storage.

