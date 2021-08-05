## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:7eceba5f58ed89f16756e5c8ff79e33d221ed64de4c9f838e22428cf02c59eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull mongo@sha256:30189d5c9e173d817875dc5e4ead0d911a8d8712bae8b18c1955a8e7bb31129f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334196846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e76511c2fcf417654d0120093fbb1f3eafd2de6475134037168b9ce1753892`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 01:23:41 GMT
SHELL [cmd /S /C]
# Wed, 14 Jul 2021 01:23:44 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 01:24:39 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 Jul 2021 01:24:40 GMT
USER ContainerUser
# Wed, 14 Jul 2021 01:24:44 GMT
COPY multi:0196f9e96f60ad3e2b92fd0773f8d0fe3a8235e1eefbb9ef1a1f0d672e6a711c in C:\Windows\System32\ 
# Thu, 05 Aug 2021 00:22:08 GMT
ENV MONGO_VERSION=4.4.8
# Thu, 05 Aug 2021 00:22:32 GMT
COPY dir:81cf8e690ba923e7a0afccbc51cca936d747bbc37074186034927b304cbda9ce in C:\mongodb 
# Thu, 05 Aug 2021 00:22:59 GMT
RUN mongo --version && mongod --version
# Thu, 05 Aug 2021 00:23:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 05 Aug 2021 00:23:03 GMT
EXPOSE 27017
# Thu, 05 Aug 2021 00:23:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5307d56ac81f33a647e0ed6f4e0f70a39b207469fe0a28ab1b9f9379669e02b4`  
		Last Modified: Wed, 14 Jul 2021 02:04:59 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a611bf59a988b0a5edd06e25ae07583657165333b55f3f7591f225964532c294`  
		Last Modified: Wed, 14 Jul 2021 02:04:59 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e35563eb5bf880fe10ab1cac2d96621bb2821366f761cb76ab30d8bb3aa1463`  
		Last Modified: Wed, 14 Jul 2021 02:04:57 GMT  
		Size: 66.6 KB (66629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b09241ae500a15f03f3c5e117bcfa73142ca23eafad6e31850d18aae5d11779`  
		Last Modified: Wed, 14 Jul 2021 02:04:56 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5c146eb6617702bbcff62dc5eec3d43581bd5388fb1c2a75c9d69a7ac66470`  
		Last Modified: Wed, 14 Jul 2021 02:04:56 GMT  
		Size: 274.0 KB (274011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9c2951669a4d0bbd1f1282d3c2a2db75289178e251f7dd0da212b329f69298`  
		Last Modified: Thu, 05 Aug 2021 00:30:44 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3550e608e9216eb9a862b7de1356066ec015984e02f47f8ff8c7b4a742b27f77`  
		Last Modified: Thu, 05 Aug 2021 00:31:20 GMT  
		Size: 231.1 MB (231054769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014d83336726c207a1537e321026a5923f165cea9cc9fd3340f62877d271d572`  
		Last Modified: Thu, 05 Aug 2021 00:30:41 GMT  
		Size: 67.7 KB (67717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d130109e500a1dd709f11f54bc677b8932b6c10b5794fc0915c7da9e1de24bc`  
		Last Modified: Thu, 05 Aug 2021 00:30:41 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da45ab3d1e9da09435ad07843a8c537fddc74200b4e77e64ebc50c49549c668b`  
		Last Modified: Thu, 05 Aug 2021 00:30:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09da6ededdb6107494421a6dd4935949bfd07a564927f0cf7063e5186be1892c`  
		Last Modified: Thu, 05 Aug 2021 00:30:41 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
