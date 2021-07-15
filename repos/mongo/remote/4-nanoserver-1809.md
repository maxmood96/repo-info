## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:55674081c06a5ab46bd949dd0fb33ef8248915d73fdd3370916da60d65ed1ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull mongo@sha256:5574a6967b8b9431c4b2ce1dc6ca56416049809522b5551ea6f426cfbf7aa0a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.8 MB (333801579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6c1c7c4cd39a3cd9aad653d3f5c9b26639d6a7b9da98acf87d5efcd7d5466e`
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
# Wed, 14 Jul 2021 01:42:45 GMT
ENV MONGO_VERSION=4.4.6
# Wed, 14 Jul 2021 01:43:08 GMT
COPY dir:e5731845368f7299600736cac7a9579787821dfbdc9d4f89336700f23196d727 in C:\mongodb 
# Wed, 14 Jul 2021 01:43:38 GMT
RUN mongo --version && mongod --version
# Wed, 14 Jul 2021 01:43:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Jul 2021 01:43:43 GMT
EXPOSE 27017
# Wed, 14 Jul 2021 01:43:46 GMT
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
	-	`sha256:abf1d238b1d9774fb70d6ca764eb67e9afd2b978394d87a8717f0f2ba26f72e3`  
		Last Modified: Wed, 14 Jul 2021 02:18:31 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30b871a97322c897a539e998de993c2d2a69aaad2e0d79da3d17553c82cd1d4`  
		Last Modified: Wed, 14 Jul 2021 02:19:17 GMT  
		Size: 230.7 MB (230658774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3064831ffdea05829fd04b042336d24fdbd0aaa04ecac5691ce3c0cc319a7fd2`  
		Last Modified: Wed, 14 Jul 2021 02:18:28 GMT  
		Size: 68.4 KB (68412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba3cad5312b37eabbb2260e7dba578e3d7ec1a0dea30c4ecf7a6829244014b9`  
		Last Modified: Wed, 14 Jul 2021 02:18:28 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2eac2ad8b88bb87ff8879a3e046dc90b8d8b33184c5eff31c50d21627a9133`  
		Last Modified: Wed, 14 Jul 2021 02:18:28 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e01c7455937b94a8867d44802710d97b218d2be8c90017a0720b3af39d66bd`  
		Last Modified: Wed, 14 Jul 2021 02:18:28 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
