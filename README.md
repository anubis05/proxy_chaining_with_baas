# proxy_chaining_with_baas

There are two proxies.
The chained_proxy_to_baas exposes the actual apis like hotels api,schools api,weathers api etc. whatever it need to be.
All the data which thie proxy serves up is stored in BaaS.
But this proxy do not talk to the BaaS.

Instead this proxy talks to the apiusergrid proxy. apiusergrid is configured to talk to BaaS.

Advantage: There can be multiple proxies which all need to talk to BaaS. The access logic is encapsulated in one proxy.

The apiusergrid proxy has caching built in. So the BaaS data is stored in apiusergrid cache thus improving performance. 
