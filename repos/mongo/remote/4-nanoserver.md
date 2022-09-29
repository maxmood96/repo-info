## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:3fc9fa3b6101140729854cbc8be56ed297732b106fa8ab169f9f678b2a8b09a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.1006; amd64

```console
$ docker pull mongo@sha256:77fcb8666f259ed6cbd1f7ead33017506b81a75cd35907535b96249b836dc3e0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.8 MB (362778068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba55c7b567ec077ff76a61b6e0cc21c62a8a815c343dad94477178fbc550764`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 12:59:22 GMT
SHELL [cmd /S /C]
# Wed, 14 Sep 2022 18:16:41 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 18:16:54 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 Sep 2022 18:16:54 GMT
USER ContainerUser
# Wed, 14 Sep 2022 18:23:48 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Thu, 29 Sep 2022 20:35:25 GMT
ENV MONGO_VERSION=4.4.17
# Thu, 29 Sep 2022 20:35:49 GMT
COPY dir:cdbba282fa1cacd2b09d4c40c2e879c5f3979f218aaa5472d9e47359ab0a3a21 in C:\mongodb 
# Thu, 29 Sep 2022 20:36:04 GMT
RUN mongo --version && mongod --version
# Thu, 29 Sep 2022 20:36:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 29 Sep 2022 20:36:05 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 20:36:06 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66db2526be0f06c7bd6ba20bdc126ca2d5645acfeb41b5784e4664de37e72b49`  
		Last Modified: Wed, 14 Sep 2022 13:25:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f7ad598d1a94ba1f1296571a4da5bf04dde81c7c49e4007c0d7536a959195b`  
		Last Modified: Wed, 14 Sep 2022 19:02:01 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a642c0d7ab9ac57ad706b35c64d641cfc15ba1205447d6102442e8658f3711`  
		Last Modified: Wed, 14 Sep 2022 19:01:59 GMT  
		Size: 99.3 KB (99284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a88827dbafc40e378d95f1d1d7f0924c103f97c9f4ceff294cc2d0eea393aba`  
		Last Modified: Wed, 14 Sep 2022 19:01:59 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bccb161631572ecd27c567a9f0ef6e1146fbc6093ddb42af4f6b8b55eb929a`  
		Last Modified: Wed, 14 Sep 2022 19:07:35 GMT  
		Size: 263.5 KB (263532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7cf80d0b1606896427d0be49bcbab4b7cdb13f9955fedb091f82aa019e09a6`  
		Last Modified: Thu, 29 Sep 2022 20:53:35 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59116a81d7763f4228262f67fb18690a2bb5024338de3de5a8c48976b2e8ed0d`  
		Last Modified: Thu, 29 Sep 2022 20:54:15 GMT  
		Size: 244.2 MB (244210431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f717821f7ecde472793ec47d67e386ff794c80b30887f30ab017062c4ee3fa5`  
		Last Modified: Thu, 29 Sep 2022 20:53:33 GMT  
		Size: 65.4 KB (65443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9a726f52bf61e218621574a39d8196f277d01d0034e727908944c0b91ae818`  
		Last Modified: Thu, 29 Sep 2022 20:53:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2941df219dba811f9127277a3fea3f80ef8c3c365458b75008a4ae3706d1c5ca`  
		Last Modified: Thu, 29 Sep 2022 20:53:33 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b57a3f79619f60089ee25de2240e0891aa48ee35e9ab58447c3d158a2f61d01`  
		Last Modified: Thu, 29 Sep 2022 20:53:33 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.3406; amd64

```console
$ docker pull mongo@sha256:466246e7e919f61e68ccf65c34baca93843819e664e48200f3c1fdf072fb8ffd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (347960247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04c7d730d36b2436b023cbd0f30d58bac852ffa3b3e6f7267a4a4c6d0a6f8a2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 13:03:35 GMT
SHELL [cmd /S /C]
# Wed, 14 Sep 2022 18:18:09 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 18:18:21 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 Sep 2022 18:18:22 GMT
USER ContainerUser
# Wed, 14 Sep 2022 18:24:40 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Thu, 29 Sep 2022 20:36:17 GMT
ENV MONGO_VERSION=4.4.17
# Thu, 29 Sep 2022 20:36:43 GMT
COPY dir:cdbba282fa1cacd2b09d4c40c2e879c5f3979f218aaa5472d9e47359ab0a3a21 in C:\mongodb 
# Thu, 29 Sep 2022 20:36:57 GMT
RUN mongo --version && mongod --version
# Thu, 29 Sep 2022 20:36:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 29 Sep 2022 20:36:58 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 20:36:59 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0668477bacdfc2e7df1cd4268b246175ed9b30cf07ccb4bcfcb258d8bee830e`  
		Last Modified: Wed, 14 Sep 2022 13:26:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ada06039b3dceb53c91ed6d7bd2d77d0abd90acba1883744d947d1ccee8349`  
		Last Modified: Wed, 14 Sep 2022 19:03:38 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d170c6bf2fd2a53a952e69b17f97ce92dd39dd7294e4b1c6ae6e11adc613210`  
		Last Modified: Wed, 14 Sep 2022 19:03:36 GMT  
		Size: 69.7 KB (69673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d16b6830f5e893640af2e263523f5ff88334d46d1a2d69d91cddf1f70f62790`  
		Last Modified: Wed, 14 Sep 2022 19:03:36 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98574a2f866f60f51f05d43d7e4e9d7e62e346b27ff83266400261170b141e2b`  
		Last Modified: Wed, 14 Sep 2022 19:08:41 GMT  
		Size: 263.5 KB (263502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc0645cfae75a67082c85e48b2a59df8e02a0992362fd4bc7b7e1f9d2bf6fab`  
		Last Modified: Thu, 29 Sep 2022 20:54:30 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9383f59399be2b88e15698b1ca5744a94cd0abda96340c153bf0cd912f04a28`  
		Last Modified: Thu, 29 Sep 2022 20:55:10 GMT  
		Size: 244.2 MB (244210408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658b8de6755dcb14a652e0ee471ade9e1f4c5d10a77ef1600c505e52a4a0dba3`  
		Last Modified: Thu, 29 Sep 2022 20:54:28 GMT  
		Size: 74.6 KB (74614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d43a1de62cc818daed8aee4f9160347b2ed0558e197396813a3c84011952ef0`  
		Last Modified: Thu, 29 Sep 2022 20:54:28 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd187dbce5aea9b30e959d01c2175deccbd4b64456fb174118af7dcd3a372709`  
		Last Modified: Thu, 29 Sep 2022 20:54:28 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1c1096ba1e4070c47d50f2fb799bf07af2149172f4789e850553dd09827b89`  
		Last Modified: Thu, 29 Sep 2022 20:54:28 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
