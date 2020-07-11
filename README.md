# Base python3 container for webapps with static content support.

## Purpuse
Serve python webapps with some static files from completly 
stateless environment like Google Cloud Run service. 

## Why
It turns out that nginx loves writing things to disk and it's very 
hard to convince it to be completely stateless. Same thing happens 
to Supervisor. Luckily, we can serve python webapps using uwsgi 
which has an option to serve static files. Note that you 
we assume we have a load balancer in front of our webapp.
