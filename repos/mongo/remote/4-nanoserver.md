## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:42c99f5934626e305cc2e6b89d594b94e0071c4ecb0bf591f6be0db05ec804cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1970; amd64
	-	windows version 10.0.17763.4851; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.1970; amd64

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

### `mongo:4-nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull mongo@sha256:e5776b124a5bc396722c39e3a66c5ba3faa92d6927d798eeba0f3a84f10d5731
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349273634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938b44ed815ef89dec8a15af1bc0a5514415540e61b8a0ec71560fb74aaddd1b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 01:47:57 GMT
SHELL [cmd /S /C]
# Wed, 13 Sep 2023 04:01:38 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 04:01:43 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Sep 2023 04:01:44 GMT
USER ContainerUser
# Wed, 13 Sep 2023 04:22:12 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Tue, 03 Oct 2023 01:30:31 GMT
ENV MONGO_VERSION=4.4.25
# Tue, 03 Oct 2023 01:30:52 GMT
COPY dir:d9377f6d4478606f95c555c570b428a952f33c4cef65b0639747b7ce806fb2fa in C:\mongodb 
# Tue, 03 Oct 2023 01:31:02 GMT
RUN mongo --version && mongod --version
# Tue, 03 Oct 2023 01:31:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 03 Oct 2023 01:31:03 GMT
EXPOSE 27017
# Tue, 03 Oct 2023 01:31:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bbcbc05a0b3c240fc185ae93c7d844ad01c0d60ef9429ad4d230a78065a9ce`  
		Last Modified: Wed, 13 Sep 2023 02:18:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8461d082f0027d9ed1cd74ee8e9e1dbcb1250ea330332f1459c3a74a59e242`  
		Last Modified: Wed, 13 Sep 2023 04:39:52 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d24e4e27b8237cb6af207bc6c651cf8397fd4f0bd0e14d7fea42327ea04aa6`  
		Last Modified: Wed, 13 Sep 2023 04:39:51 GMT  
		Size: 70.2 KB (70185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0a145cf1519e52c048521ae1f199df2b6cba60425d6ed0fda7071a4785269e`  
		Last Modified: Wed, 13 Sep 2023 04:39:51 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9a3648bd9e446adfa30a5a41133aedd1a84e0ac88bb23fc3d50edffd64ba03`  
		Last Modified: Wed, 13 Sep 2023 04:55:15 GMT  
		Size: 263.4 KB (263400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b34cceaa30ef772ce8794192002273f0986cf4360ee35b605674ea7d7cabce2`  
		Last Modified: Tue, 03 Oct 2023 02:32:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e3af34e95b761e27cbf29f1505d7a79ab42a97b82312b546a655c5af9c0458`  
		Last Modified: Tue, 03 Oct 2023 02:33:39 GMT  
		Size: 244.4 MB (244395161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c4ba007d670af4a6617e4083e496a8ed6d4a03707980de81c3845bcf99f09e`  
		Last Modified: Tue, 03 Oct 2023 02:32:56 GMT  
		Size: 44.6 KB (44551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5f299104a052d6037ded8495f96491c02a2b75c2d8cc7f7f2b865daf1d6530`  
		Last Modified: Tue, 03 Oct 2023 02:32:55 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769c76f302593cf9a42429ef26ea9b5b716aebd3b9dccc53212025dc97c4aa6`  
		Last Modified: Tue, 03 Oct 2023 02:32:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f586c17f03997745d8638e1842a0e0260dc41d9067974cb4ea7f00df377f3db3`  
		Last Modified: Tue, 03 Oct 2023 02:32:56 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
