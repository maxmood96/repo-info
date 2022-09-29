## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:06ba4cf0d9f65693607d199b4d42aceb54f722feaeda1f8173f5eb6375c79929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.3406; amd64

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
