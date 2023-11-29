## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:0fc4e3e80002090f55cfa2f83007c034ad216bd385d2c8110261b89e515a17b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull mongo@sha256:e7e970d88639a2600f92063f96f97d11b42ebc91c0e1a8c5794e384007e0a546
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349338708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ab2dcf9cbf52ac11c1fb7968ef5291d0f0d1834ff31c801cf32a65d8a0b165`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 02:55:52 GMT
SHELL [cmd /S /C]
# Thu, 16 Nov 2023 03:26:22 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 03:26:36 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 16 Nov 2023 03:26:36 GMT
USER ContainerUser
# Thu, 16 Nov 2023 03:57:55 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 29 Nov 2023 01:45:29 GMT
ENV MONGO_VERSION=4.4.26
# Wed, 29 Nov 2023 01:45:53 GMT
COPY dir:c994cd7865d1b394f7e8a8c4a110ab2ce4ac2888cb8ffc9938a14314ee791f72 in C:\mongodb 
# Wed, 29 Nov 2023 01:46:06 GMT
RUN mongo --version && mongod --version
# Wed, 29 Nov 2023 01:46:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 Nov 2023 01:46:07 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 01:46:08 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26eb16ff47ed3c1f3ff64a9920a3407afa035ee398f803b948326dc0e5e4e79e`  
		Last Modified: Thu, 16 Nov 2023 03:13:07 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e02f563a12fbc6846cdd83dd195b52331a6b956d0cadd546aac9d48eafc857c`  
		Last Modified: Thu, 16 Nov 2023 04:24:41 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67c125c9a773e11ea7d5d4837aab6edb57a3542f5d40eb33917ff54a1764254`  
		Last Modified: Thu, 16 Nov 2023 04:24:39 GMT  
		Size: 68.4 KB (68440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ebb2a529df887c3f03501c0eb37994d3377f525a469a8ec60551d78b6fa67f`  
		Last Modified: Thu, 16 Nov 2023 04:24:38 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3c7cbc119978d3d4f1dea0cf8fa98065d456932d1c14d27637e965347f8383`  
		Last Modified: Thu, 16 Nov 2023 04:48:59 GMT  
		Size: 263.4 KB (263376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de7c5f1fd6f3d8b6593ee0a516e0912089ba6997f0abc1e7b4b738eb73263d7`  
		Last Modified: Wed, 29 Nov 2023 02:09:25 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4651bdda3e2f77edf83b5b8c06fa5bdd7fb7841f37c9bfd3ea57718ba4de1a1a`  
		Last Modified: Wed, 29 Nov 2023 02:10:09 GMT  
		Size: 244.4 MB (244413728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9776de71a1b57631c6c041b82bf29a83e53aa07f6f810bdcd33c3a288031c9`  
		Last Modified: Wed, 29 Nov 2023 02:09:24 GMT  
		Size: 88.0 KB (88040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bac82c3fc9ee29e072ec1d308cdbc51202b3073f882664eed6dd1f08d90ca0`  
		Last Modified: Wed, 29 Nov 2023 02:09:23 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1aa3fb646afe02547ec3f203c0d6574b838f19e307e3b88d4ec1d51c210a16`  
		Last Modified: Wed, 29 Nov 2023 02:09:24 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a79fa9243dfaa76fbc5cae4dd39c5fbb9c74ea595141c8f0e58d13f3ba8d6c`  
		Last Modified: Wed, 29 Nov 2023 02:09:24 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
