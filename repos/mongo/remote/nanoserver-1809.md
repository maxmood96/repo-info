## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:8546e78a3620784be54ae005f82a1f0b4ab145f40a6a622cb30b73063f6e5dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull mongo@sha256:eebf90422ba916295734cdded5ee55922b3392d8bb799244b982fa4a1f802ad8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 MB (397383282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38315907dadb66386570c1e30cc34fc1c9c728c5397af3bfe951fa2359a1ec8a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 13:19:53 GMT
SHELL [cmd /S /C]
# Wed, 12 Jan 2022 16:41:35 GMT
USER ContainerAdministrator
# Wed, 12 Jan 2022 16:41:49 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Jan 2022 16:41:50 GMT
USER ContainerUser
# Wed, 12 Jan 2022 16:41:51 GMT
COPY multi:0196f9e96f60ad3e2b92fd0773f8d0fe3a8235e1eefbb9ef1a1f0d672e6a711c in C:\Windows\System32\ 
# Wed, 12 Jan 2022 16:41:52 GMT
ENV MONGO_VERSION=5.0.5
# Wed, 12 Jan 2022 16:42:54 GMT
COPY dir:97e0851993a8443e809dbfb982fa612becf2ad4c3b07d76c242613492af3987d in C:\mongodb 
# Wed, 12 Jan 2022 16:43:23 GMT
RUN mongo --version && mongod --version
# Wed, 12 Jan 2022 16:43:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jan 2022 16:43:24 GMT
EXPOSE 27017
# Wed, 12 Jan 2022 16:43:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e33ce14c030f51993f87b8caf6fcbc38d7e0c720e938c28109df0cc1fcecc69`  
		Last Modified: Wed, 12 Jan 2022 13:45:07 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8939f342fed44c2788bbad268cc1694d0f7847a41cfe6de812fcddbe3bfa5b1d`  
		Last Modified: Wed, 12 Jan 2022 17:25:09 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63721e629e6b8e03acc500ea84ead467fb1d34524b70a07e8f1aee67bc571055`  
		Last Modified: Wed, 12 Jan 2022 17:25:07 GMT  
		Size: 78.0 KB (78013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fc02788fb3893cd4e6cde670b7e4bb3af946e8912d384ebf2ed584cdd09e50`  
		Last Modified: Wed, 12 Jan 2022 17:25:07 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a88a4399879d6cc0c2bab8adf64257dde87a874c8af0abefeaf548b55d55c0`  
		Last Modified: Wed, 12 Jan 2022 17:25:08 GMT  
		Size: 274.1 KB (274092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26ff52f41e6e5cf10bc32d02cf5b256313640fc2c63d393f15b155a659d54ab`  
		Last Modified: Wed, 12 Jan 2022 17:25:07 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2834e1812062ff311f8eac7e241e4f127e9f023e135b2b5e9ed1907469506e`  
		Last Modified: Wed, 12 Jan 2022 17:26:00 GMT  
		Size: 293.9 MB (293935599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e53ae1ba79385eef9fa16ae869c79f9e25bf58d4a93e3b083b5c903d541c92`  
		Last Modified: Wed, 12 Jan 2022 17:25:05 GMT  
		Size: 56.4 KB (56413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8606ce1d48e9b3480e78b4b04e60aa5feb204b1469da58a243ec42da400292ca`  
		Last Modified: Wed, 12 Jan 2022 17:25:05 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f57ae8dfa2915dc1d045cd82db139d00d2c8040bcd657ff4577de1f622e6e7`  
		Last Modified: Wed, 12 Jan 2022 17:25:05 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f91678718fc4bab28fe07ba582efc1a9e3aefd80518b70766726c19516cb4d`  
		Last Modified: Wed, 12 Jan 2022 17:25:05 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
