## `gazebo:latest`

```console
$ docker pull gazebo@sha256:b0c1a6638ac9a61f49611641144b1b19fa3cb16ef52aa50ef17a129441a1eb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:latest` - linux; amd64

```console
$ docker pull gazebo@sha256:e9cd17965b4f9d2dfea880c47f77765cd04a942e365059979ce52ecc35d429a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605599585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8178ab9ceb65772649fcdb46659f9ad02e7ed74f775ac263f963181be3c758cf`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:09:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:15:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:15:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 07 Jan 2022 05:15:38 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Mon, 24 Jan 2022 19:39:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.10.1-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 24 Jan 2022 19:39:48 GMT
EXPOSE 11345
# Mon, 24 Jan 2022 19:39:49 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Mon, 24 Jan 2022 19:39:49 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 24 Jan 2022 19:39:49 GMT
CMD ["gzserver"]
# Mon, 24 Jan 2022 19:45:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.10.1-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07d6b806a5eae974734f3df21a5799c46db4c8dc12ffc6bab4a8ca2f802d1b5`  
		Last Modified: Fri, 07 Jan 2022 04:34:49 GMT  
		Size: 1.2 MB (1182238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c0bba77aa7d24282d153e2a02032e5484ee8a5ca1879eb9ff0e473a7f3ff7c`  
		Last Modified: Fri, 07 Jan 2022 05:25:43 GMT  
		Size: 16.2 MB (16169890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fadef1dc985611b2e7adc1e486b110f8d89368e6e69b7393a4f7581b354ef6`  
		Last Modified: Fri, 07 Jan 2022 05:25:40 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ae5a366fc56bde9f5c014cd333b5cd60218fddd6d1d1f03bb707df6c5acb7f`  
		Last Modified: Fri, 07 Jan 2022 05:25:41 GMT  
		Size: 5.5 KB (5502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146ac545e87f48e7b839d1cb5258e0854e9815fc94273f64317d0024a48d1bb5`  
		Last Modified: Mon, 24 Jan 2022 19:48:29 GMT  
		Size: 275.0 MB (275017147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5599a705c6b575558a6783bb9d5445d9f4a5a6aa0fc9d08d60abce079e676c1c`  
		Last Modified: Mon, 24 Jan 2022 19:48:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbc89766794d725e205034104d137426cbdf3bb556102417b1de1af45a8370d`  
		Last Modified: Mon, 24 Jan 2022 19:49:46 GMT  
		Size: 284.7 MB (284656754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
