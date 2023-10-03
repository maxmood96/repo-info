## `mongo:4-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:9a5decb1d83961f549b65a71fbebdeedbb81b99fc026503ade9a77d4c35589db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `mongo:4-nanoserver-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull mongo@sha256:9344d9c89f50e0ca2bca4217bee0fb5c6a7feef0fb9f7a372b7f637ac077dbba
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.4 MB (365374482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27bc1294627afe3807295f3da6e85d5dc7363930c9fb674b7b160a787e02e50`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 01 Sep 2023 00:20:14 GMT
RUN Apply image 10.0.20348.1970
# Wed, 13 Sep 2023 01:45:13 GMT
SHELL [cmd /S /C]
# Wed, 13 Sep 2023 04:00:25 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 04:00:30 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Sep 2023 04:00:31 GMT
USER ContainerUser
# Wed, 13 Sep 2023 04:21:27 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Tue, 03 Oct 2023 01:29:46 GMT
ENV MONGO_VERSION=4.4.25
# Tue, 03 Oct 2023 01:30:09 GMT
COPY dir:d9377f6d4478606f95c555c570b428a952f33c4cef65b0639747b7ce806fb2fa in C:\mongodb 
# Tue, 03 Oct 2023 01:30:18 GMT
RUN mongo --version && mongod --version
# Tue, 03 Oct 2023 01:30:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 03 Oct 2023 01:30:19 GMT
EXPOSE 27017
# Tue, 03 Oct 2023 01:30:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8f8cef0759210af9d01a2fb45d79956a2db738bbd3734b7244b17e14ad945cab`  
		Last Modified: Tue, 12 Sep 2023 18:47:39 GMT  
		Size: 120.6 MB (120567584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c795bb9d48e9fa247e549604525fcb2599507cf1008aa1df12036f428ea236d`  
		Last Modified: Wed, 13 Sep 2023 02:18:07 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4d4f6211677cf82e6ed0d87f108ca902b6953cac7069b26a23966ebb167924`  
		Last Modified: Wed, 13 Sep 2023 04:38:18 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409b27824df1096550781d8d27fdafeb1abf5437c93f4d7bce18fdab09d1a67c`  
		Last Modified: Wed, 13 Sep 2023 04:38:16 GMT  
		Size: 79.5 KB (79488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01ed47b78f8c73c7cb1a91613a90350ec6f08cbad9f792825e0a51f4f144fd0`  
		Last Modified: Wed, 13 Sep 2023 04:38:16 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d1c7ce100358fa46d16a3327a47a66e4351aee22769f947d1afd110e118b21`  
		Last Modified: Wed, 13 Sep 2023 04:54:11 GMT  
		Size: 263.4 KB (263377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd47b2df307353323e045a67f7ce6a563988365761cea2efbcd564a6351cd01`  
		Last Modified: Tue, 03 Oct 2023 02:32:01 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167c954d433056f70b34144c28eda8b0fe151169f4db21f15698a865510580de`  
		Last Modified: Tue, 03 Oct 2023 02:32:43 GMT  
		Size: 244.4 MB (244395142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0828797adadb34dbd6e44e01a0f745624ef2d45394ef09a79b83f3515e4ad7`  
		Last Modified: Tue, 03 Oct 2023 02:32:00 GMT  
		Size: 60.7 KB (60729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5766fd9bf90f9b261cda6f2c409d868fa081f3f7e18aad8a1ae177e3c10ff8`  
		Last Modified: Tue, 03 Oct 2023 02:32:00 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7081442e7d1d736c254703dd86aba787704c1dcda4841e2d0693f1b7d600ec`  
		Last Modified: Tue, 03 Oct 2023 02:31:59 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe2f98258b64020fde9d0e624c8270498c373306d3542890f43527d1d56d858`  
		Last Modified: Tue, 03 Oct 2023 02:32:00 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
