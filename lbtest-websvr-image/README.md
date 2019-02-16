# lbtest-websvr

Continer image with Apache and PHP that echos the running instance's current IP address on the main page.

#### Build in Docker or Pull Pre-Built Image
`cd lbtest-websvr`\
`docker build -t lbtest-websvr .` \

#### Run in Docker
`docker run -p 8080:80 -d lbtest-websvr`

#### Verify instance is reporting IP
`curl localhost:8080`

#### Stop the instance
`docker stop <CONTAINER_ID>`

#### Ship to a private registry
`docker tag lbtest-websvr <REGISTRY_FQDN>/library/lbtest-websvr:v1` \
`docker push <REGSITRY_FQDN>/library/lbtest-websvr:v1`\
`cd ..`
