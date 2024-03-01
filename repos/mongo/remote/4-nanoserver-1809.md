## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:9a6accbf831b276ab19d5a890458d0ea3e26264dcefc48cc1298c98e3de93685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull mongo@sha256:5941cbb5e7fc5eadd9c79bd4f6e4b223910cc5ff03aa067dbbb6e7280fa69583
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350337553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe87990742b5e54fd5d4308de45b7e79588f4943927a47171c8b2660b7d6f2f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Fri, 01 Mar 2024 01:50:11 GMT
SHELL [cmd /S /C]
# Fri, 01 Mar 2024 01:50:12 GMT
USER ContainerAdministrator
# Fri, 01 Mar 2024 01:50:24 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 01 Mar 2024 01:50:25 GMT
USER ContainerUser
# Fri, 01 Mar 2024 01:50:27 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Fri, 01 Mar 2024 01:50:28 GMT
ENV MONGO_VERSION=4.4.29
# Fri, 01 Mar 2024 01:50:44 GMT
COPY dir:05c527a8cd901f69ca11856f2b42c60f8bfbb1c962d124799003a0c1b4353f7a in C:\mongodb 
# Fri, 01 Mar 2024 01:50:51 GMT
RUN mongo --version && mongod --version
# Fri, 01 Mar 2024 01:50:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 01 Mar 2024 01:50:53 GMT
EXPOSE 27017
# Fri, 01 Mar 2024 01:50:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35161296f9ec7d626b899d2bce97f459ee59e202ea18f7cf2fd1c8df8da386ac`  
		Last Modified: Fri, 01 Mar 2024 01:51:02 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aaeeb4094417ba5197f1a45bba612dff28fbc7e364da6ebf46b362e296a3fbd`  
		Last Modified: Fri, 01 Mar 2024 01:51:02 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3770a93905a85a1d2274df3cf605107f01d0d24ec48a67d354f817aa72c202`  
		Last Modified: Fri, 01 Mar 2024 01:51:00 GMT  
		Size: 68.0 KB (68018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12550ce024e4ea5ff631371d9fb58d3b905b9581a9d6465156a320422594eb9e`  
		Last Modified: Fri, 01 Mar 2024 01:51:00 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ef6870ce3144844727253910858c57ad67755f3ad7c042c390d8797f3891b6`  
		Last Modified: Fri, 01 Mar 2024 01:51:00 GMT  
		Size: 267.4 KB (267416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f465400067633894d3e762fbc1952bc3a99759275e3f4fbc0bacea887811e8`  
		Last Modified: Fri, 01 Mar 2024 01:51:00 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ceefed3c1b6dca8081e92e7e95391e56287189f96af69b7365af393b023ce56`  
		Last Modified: Fri, 01 Mar 2024 01:51:23 GMT  
		Size: 245.3 MB (245305518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb049ecf909a709c49e9d65f2cef9f4132b303ba70cc0cdf3cf27faaf9082d7`  
		Last Modified: Fri, 01 Mar 2024 01:50:58 GMT  
		Size: 67.7 KB (67740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452ff7267c1992bcacba3ceed6dc84b8e96913bf747d2e133d32ec95d2e1b258`  
		Last Modified: Fri, 01 Mar 2024 01:50:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633520eb53c6aa5b8715d1f6983d82c6c34201f3dbacf1701e611844d1e88f1a`  
		Last Modified: Fri, 01 Mar 2024 01:50:58 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5fcedf0b01ea15c1b482cd5989abf1c3dfa07f1cb08442f0ad20b7b2f0691`  
		Last Modified: Fri, 01 Mar 2024 01:50:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
