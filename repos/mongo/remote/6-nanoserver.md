## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:7a5d54af30a010c9632cdcfc52a18601fd68bc7b12ee97e9b84b42d8cc316091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.2655; amd64

```console
$ docker pull mongo@sha256:4382bcbac04dd8ce79e7b4dd964b38df04d2b096b1c633e4c1442bb761da2a5b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.1 MB (644062823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935f68753b35dd31b41fb9e8e8716716ee82735fed0d96716d54f5afab13fbdb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 10 Aug 2024 19:28:00 GMT
RUN Apply image 10.0.20348.2655
# Tue, 13 Aug 2024 21:09:15 GMT
SHELL [cmd /S /C]
# Tue, 13 Aug 2024 21:09:15 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 21:09:17 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 13 Aug 2024 21:09:18 GMT
USER ContainerUser
# Tue, 13 Aug 2024 21:09:20 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 13 Aug 2024 21:09:20 GMT
ENV MONGO_VERSION=6.0.16
# Tue, 13 Aug 2024 21:09:36 GMT
COPY dir:6f4af2768a9f782f0ee6ba32759515874004eaed990f1ac643f6b3295b8b75af in C:\mongodb 
# Tue, 13 Aug 2024 21:09:46 GMT
RUN mongod --version
# Tue, 13 Aug 2024 21:09:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Aug 2024 21:09:48 GMT
EXPOSE 27017
# Tue, 13 Aug 2024 21:09:48 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:695cae91f2de8dadf81c8b3a95f4942533ef064a72ad8fa7843cca84a839bfba`  
		Last Modified: Tue, 13 Aug 2024 20:02:51 GMT  
		Size: 120.6 MB (120554921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5555562217779531213120c13692f0e8bba27b7a1e6a3dbddae12ccc0e67d764`  
		Last Modified: Tue, 13 Aug 2024 21:09:56 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675a0138941a9af12ae850e18c12a55f3988a80544b32968c1347452168afba7`  
		Last Modified: Tue, 13 Aug 2024 21:09:56 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04511b4347ff9e8f5afb49932d2163a5eb96f00daa067b857b352ace29598bf`  
		Last Modified: Tue, 13 Aug 2024 21:09:54 GMT  
		Size: 77.8 KB (77761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079aac1c89a0051f625de7056e7d91167fd90293f861555f03ce4923cb04f345`  
		Last Modified: Tue, 13 Aug 2024 21:09:54 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed99e20698dafd43b5b37957cd2b0658c16e1df1dcaddc2a1596ba6fe40ddc5`  
		Last Modified: Tue, 13 Aug 2024 21:09:54 GMT  
		Size: 275.2 KB (275172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90a8f1b1d0be30d6febc2deaff747379381b990df65471415aea6fc7ed0d078`  
		Last Modified: Tue, 13 Aug 2024 21:09:54 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2605b64b56acb7faaae5b56617b3d6b869c8b3d9856731df97df496d6d73f99a`  
		Last Modified: Tue, 13 Aug 2024 21:10:34 GMT  
		Size: 523.0 MB (523038489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c82d8e5cbb5bdc1dd998c50172514b67641e326d034e2b6cece73261b6f1458`  
		Last Modified: Tue, 13 Aug 2024 21:09:52 GMT  
		Size: 109.3 KB (109271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabab5b57164af4be6c5d5fbf35b86ad8399f7dbf425e989fd9fdf7551b21b4`  
		Last Modified: Tue, 13 Aug 2024 21:09:52 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6ed6debc9a5f2f35957b2fddb735439e55e2d36a4745dd09e18aaf54547ea3`  
		Last Modified: Tue, 13 Aug 2024 21:09:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4772b63ceffd065fad7f269bb421c64bc77644fc0f14ec4ff5e3bd4e7ff8f9a7`  
		Last Modified: Tue, 13 Aug 2024 21:09:52 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull mongo@sha256:c9dbedd3e9e9998cbddde34a82ecc3550469a9d1dde0fd90c1c84252f60e00de
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.6 MB (678562178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e68c4848c537c80fef7d9885a2b7903beb21da66c31246729f9e4cdaf5e3cd9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 21:15:36 GMT
SHELL [cmd /S /C]
# Tue, 13 Aug 2024 21:15:38 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 21:15:41 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 13 Aug 2024 21:15:41 GMT
USER ContainerUser
# Tue, 13 Aug 2024 21:15:43 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 13 Aug 2024 21:15:44 GMT
ENV MONGO_VERSION=6.0.16
# Tue, 13 Aug 2024 21:16:11 GMT
COPY dir:6f4af2768a9f782f0ee6ba32759515874004eaed990f1ac643f6b3295b8b75af in C:\mongodb 
# Tue, 13 Aug 2024 21:16:16 GMT
RUN mongod --version
# Tue, 13 Aug 2024 21:16:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Aug 2024 21:16:18 GMT
EXPOSE 27017
# Tue, 13 Aug 2024 21:16:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b31e67824225f2bec6684cbd7c7f51415bc889b8cdaffb82fa6a92c3532c79`  
		Last Modified: Tue, 13 Aug 2024 21:16:24 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35ff4897937d11fd39f8af8468cd45981a598759ea377472a3bc0bc0b005c11`  
		Last Modified: Tue, 13 Aug 2024 21:16:24 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3e5ddb5326fbe4ac8b106e55a993dc13723edd4ebb64196289a37806496d22`  
		Last Modified: Tue, 13 Aug 2024 21:16:23 GMT  
		Size: 71.5 KB (71460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16490ed8475bc2d5de05b8ca82646644c6b1f21970eba51d2031e1ec2de388a0`  
		Last Modified: Tue, 13 Aug 2024 21:16:23 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22f838f02904b1dce697de0db9059e2dd8d2d1d75186558c37a3e778f432b81`  
		Last Modified: Tue, 13 Aug 2024 21:16:23 GMT  
		Size: 275.2 KB (275172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d27b05560c6f516257866f1b35b6ec457f4259143fe5a9ec11f1984eddc4b7c`  
		Last Modified: Tue, 13 Aug 2024 21:16:23 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d95a805fe8dede543f80fe7b201e37d04b1d149f3b021e328f3d604deca925`  
		Last Modified: Tue, 13 Aug 2024 21:17:04 GMT  
		Size: 523.0 MB (523038463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ed93fbaac965610e57b9c3e79c88b7651a2cb6eea6c9624b9b8a8195a83dae`  
		Last Modified: Tue, 13 Aug 2024 21:16:22 GMT  
		Size: 86.7 KB (86712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6204a8b175a80d5c9fbe9bcb2d864a98ae6ac52705047525844976f4f04c1d42`  
		Last Modified: Tue, 13 Aug 2024 21:16:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9953a9f05e3d5c700f5164fe995751d3c310997f3008a3c972ab415813e2c42b`  
		Last Modified: Tue, 13 Aug 2024 21:16:22 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03761bc060f6542856584a12a0dfbe917f52405efbfe516857c9b1f57a4e8c4`  
		Last Modified: Tue, 13 Aug 2024 21:16:22 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
