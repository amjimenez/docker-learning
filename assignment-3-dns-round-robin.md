# DNS Round Robin(RR) Test

:whale:

Requirements:

- know how to use it to get shell in container
- Understand basics of what a linux distribution is like Ubuntu and CentOS
- Know how to run a container
- Understand basics of DNS records

Two different host that response to the same dns name

Ever since Docker Engine 1.11, we can have multiple containers on a
created network respond to the same DNS address.

[X] Create a new virtual network (default bridge driver)

`$ docker network create my_example`

[X] Create two containers from elasticsearch:2 image & Research and use
--network-alias search when creating them to five them and additional DNS name
to respond to

`$ docker container run -d --net my_example --net-alias search elasticsearch:2`
`$ docker container run -d --net my_example --net-alias search elasticsearch:2`

[X] Run alpine nslookup search with --net to see the two containers list for the same DNS name

`$ docker container run --rm --net my_example alpine nslookup search`

[X] Run centos curl -s search:9200 with --net multiple times until you see both "name" fields show

`$ docker container run --rm --net my_example centos curl -s search:9200`
