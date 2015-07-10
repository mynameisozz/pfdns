This project is developed for multihomed host to get optimized DNS query result. The term "multihomed host" means that there are multiple upstream ISP's connected with this host.

pfdns is supposed to work with customized routing table, and it assumes that user has already configured the routing table such that the connection speed is optimized.

Assume that each ISP's recursor provides the optimal DNS result for its network, but in some cases it's better choosing one ISP than the other ISPs to reach the destination site. So that user may want to select the best one among all the DNS query results from the upstream DNS's, according to some policy. It's often useful when a target website provides different IP's to connect (CDN) for different region or ISP, and some ISP has better quality while accessing this site.

pfdns is developed on the basis of libunbound and unbound. Benifited from async resolving, caching of libunbound and modular design of unbound, the extra work besides the key logical part of pfdns is minimized.