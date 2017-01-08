## Useful Resources 

1. Download docker file for quickstart cloudera

```
https://www.cloudera.com/documentation/enterprise/5-6-x/topics/quickstart_docker_container.html
```

2. Install docker file 

```bash
docker pull cloudera/quickstart
docker images # to make sure image is installed
docker run --privileged=true --hostname=quickstart.cloudera -p <port>:8888:8888 -t -i <image> /usr/bin/docker-quickstart
```

3. In order to install on laptop directly:

   1. Tutorial : http://zhongyaonan.com/hadoop-tutorial/setting-up-hadoop-2-6-on-mac-osx-yosemite.html 
   2. Unable to find scheduler : https://github.com/saltstack-formulas/hadoop-formula/issues/18



