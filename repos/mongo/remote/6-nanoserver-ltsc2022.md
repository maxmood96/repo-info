## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:da01634670f11b535a74c28c6f76744c11ac6b346364574feaf4136a21c422db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull mongo@sha256:b96ec4c8737915f2e977ef47e3fba22eb9af1af4e662b635bf1a95a4e609937e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.9 MB (648907150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d01e930b4c5422b8a3384055b42d7b2084a7975d9331caad1e8db2d6ba71aee`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:19:36 GMT
SHELL [cmd /S /C]
# Tue, 10 Jun 2025 22:19:37 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:19:39 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 10 Jun 2025 22:19:40 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:19:42 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 10 Jun 2025 22:19:42 GMT
ENV MONGO_VERSION=6.0.24
# Tue, 10 Jun 2025 22:20:00 GMT
COPY dir:cba4e76c3274759dc0518bf251e036b8561f41ea07b83e09dbbba9a2cc67c594 in C:\mongodb 
# Tue, 10 Jun 2025 22:20:11 GMT
RUN mongod --version
# Tue, 10 Jun 2025 22:20:13 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Jun 2025 22:20:14 GMT
EXPOSE 27017
# Tue, 10 Jun 2025 22:20:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68fc8f1037b0fddd20114275a301f661e5be684cfac68d19e0a177d8c941a62`  
		Last Modified: Tue, 10 Jun 2025 22:33:09 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b4d6a208b834908e1545d9ce1ff6daff51b7e44887394610b1758570c15299`  
		Last Modified: Tue, 10 Jun 2025 22:33:12 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2085c713f21bb01f8d958e78f0efdbc4b381bcecec39525f0ad8ff7d488d0909`  
		Last Modified: Tue, 10 Jun 2025 22:33:16 GMT  
		Size: 77.0 KB (76967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944dd2102b6fe0ee4c93874d92731239289a53a4598a459aae4917837dee872c`  
		Last Modified: Tue, 10 Jun 2025 22:33:19 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afffb0cc92e33186800bafc626d19158720d5c828ba14dd673eeb4f00c6bfc1`  
		Last Modified: Tue, 10 Jun 2025 22:33:22 GMT  
		Size: 275.2 KB (275153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf161b39f734c95a534c82156831c7437e82b888b013e8ded132c0c37df3e91`  
		Last Modified: Tue, 10 Jun 2025 22:33:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a40cc5a19127b9487d40bf3e30a2deba48fefb625cd00df51be24ee0a22184d`  
		Last Modified: Wed, 11 Jun 2025 01:07:51 GMT  
		Size: 525.9 MB (525908242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4e1b5fc0f8e2e0b73a91d33c72ced604b48ad49aaf36e3a0f71ddc5759e7e3`  
		Last Modified: Tue, 10 Jun 2025 22:33:29 GMT  
		Size: 98.9 KB (98913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230625b85935febb07f5a7eafab9941150615763aeb945c3b9b3adcec62b4439`  
		Last Modified: Tue, 10 Jun 2025 22:33:34 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5f1cd58b59297ee18983dfaaf7436ba25353d6b96387a92f03175998dfb50`  
		Last Modified: Tue, 10 Jun 2025 22:33:36 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09420d1ffa2bbb1c189aa323f5805713045ba260c1f790ccdd4c7dfbf15e248`  
		Last Modified: Tue, 10 Jun 2025 22:33:39 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
