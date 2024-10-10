## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:f8c521a9c42f0c9f799e8e55acca65a87d8dc216eaac0622532bdc1c389480eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull mongo@sha256:74ad78ff801f1646a24f2be797e3698bd0ce52ac8a20e5f1af53714a8d41861d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.6 MB (644611998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41201e534ac0222a81bd87223515bfe0791ff7be299d57b55db1ebfd728b3e5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:01:05 GMT
SHELL [cmd /S /C]
# Thu, 10 Oct 2024 00:01:06 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:01:08 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Oct 2024 00:01:09 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:01:10 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 10 Oct 2024 00:01:11 GMT
ENV MONGO_VERSION=6.0.18
# Thu, 10 Oct 2024 00:01:31 GMT
COPY dir:340f26541b74bac93fbc0306b4a24bb66227c5b0b1968f013d1e5b14ef125ee7 in C:\mongodb 
# Thu, 10 Oct 2024 00:01:42 GMT
RUN mongod --version
# Thu, 10 Oct 2024 00:01:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Oct 2024 00:01:43 GMT
EXPOSE 27017
# Thu, 10 Oct 2024 00:01:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59502525197d1b8b8016413acbfa085ac33778b2ad87f162a258e73cefd9b7b5`  
		Last Modified: Thu, 10 Oct 2024 00:01:52 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab231bd5ce41f931a465029027fc3174961feee65f913a6ba6824eadbc3fc50`  
		Last Modified: Thu, 10 Oct 2024 00:01:52 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0ab7a77ea5ed61cdf45cfe66b94fbba9b113216e22eca4e13e387c6da46443`  
		Last Modified: Thu, 10 Oct 2024 00:01:50 GMT  
		Size: 77.4 KB (77420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd32c1e55cfb4413d670dc7e46ca1169a6c1fb2581a7ba52306780b4befa793`  
		Last Modified: Thu, 10 Oct 2024 00:01:50 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9015878c292cda00992dcf19f4d715e1e8fb6ed5e5f37b7c7e49d4a7d3f2eb8d`  
		Last Modified: Thu, 10 Oct 2024 00:01:50 GMT  
		Size: 275.1 KB (275149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c95a145414c8c7fb3ac81c800d696c078ff6fea7b631b89e0e7b1039b7df24`  
		Last Modified: Thu, 10 Oct 2024 00:01:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78737f406353b2454b97c581b865a9266fb88e6050387d24def732561a26253`  
		Last Modified: Thu, 10 Oct 2024 00:02:29 GMT  
		Size: 523.6 MB (523631596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37237767236be4faeef645e3e7ab21a2d8d80d96ab28d81f27ad359af5c3321`  
		Last Modified: Thu, 10 Oct 2024 00:01:48 GMT  
		Size: 109.6 KB (109613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a59bfa4b13cc005dc4e152c8f3cb85b95ff654c96963565538c7307c4a8651f`  
		Last Modified: Thu, 10 Oct 2024 00:01:48 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98a01c475e758468d427bcceee961a52056b78266eb2403bc9828893b123c3f`  
		Last Modified: Thu, 10 Oct 2024 00:01:48 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2ef156a360d41b1944cc19ee1d14cf343bc5ddc5776540693ea05c1923f738`  
		Last Modified: Thu, 10 Oct 2024 00:01:48 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:70f407d1f40a1c16442a3c89187eb8e58949b9120399be4566452c1f391da00d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.2 MB (679161587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea7fe9a6199d1bae25cf6bd6937a114aae680f060b4cace33c562048f9f4492`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:02:55 GMT
SHELL [cmd /S /C]
# Thu, 10 Oct 2024 00:02:57 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:02:59 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Oct 2024 00:03:00 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:03:01 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 10 Oct 2024 00:03:02 GMT
ENV MONGO_VERSION=6.0.18
# Thu, 10 Oct 2024 00:03:29 GMT
COPY dir:340f26541b74bac93fbc0306b4a24bb66227c5b0b1968f013d1e5b14ef125ee7 in C:\mongodb 
# Thu, 10 Oct 2024 00:03:35 GMT
RUN mongod --version
# Thu, 10 Oct 2024 00:03:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Oct 2024 00:03:36 GMT
EXPOSE 27017
# Thu, 10 Oct 2024 00:03:36 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832c9655cb464f78fd43cc1867f31fac7edfa5f7e9130ab5c77412c00f8bb7f1`  
		Last Modified: Thu, 10 Oct 2024 00:03:41 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042b6a2cd6e054a60851e175dfa42aa254b71ece6c4ad60f9db583350b36bf80`  
		Last Modified: Thu, 10 Oct 2024 00:03:41 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2c9c6a3dd2d1c5779b2bab082c1ec490846229d5ba471b2afb5de7211ed331`  
		Last Modified: Thu, 10 Oct 2024 00:03:40 GMT  
		Size: 76.0 KB (76010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7537237f02af85709fffc6c62b2f1aaaf3652cb489965718a22bcf2fccc70568`  
		Last Modified: Thu, 10 Oct 2024 00:03:40 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09aca368338b21cf000f4906575cd49fec1aecf5e53e4e15dba256c4e5bf804c`  
		Last Modified: Thu, 10 Oct 2024 00:03:40 GMT  
		Size: 275.2 KB (275170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750c5ef98536943fa163e3e5db0f8635ce26f8a1f438652e05bc07f6fdeffd8a`  
		Last Modified: Thu, 10 Oct 2024 00:03:40 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fce89053fd650a17ed1b60978eb49a2797441c90c5903ffc60a86a583410abb`  
		Last Modified: Thu, 10 Oct 2024 00:04:20 GMT  
		Size: 523.6 MB (523631550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a6e5ad91532835e61c65c9652f39fc4544b45a827894676f0b1d1f8b8d9edd`  
		Last Modified: Thu, 10 Oct 2024 00:03:39 GMT  
		Size: 78.0 KB (78011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac1006afa3b94e7e18680f248a4d9e419758e3a950739c651e211a6e6f44741`  
		Last Modified: Thu, 10 Oct 2024 00:03:39 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba812887423c83f2dec1e4b5e0e3de387f5e68eeb83153af93d9d8124b1c37bb`  
		Last Modified: Thu, 10 Oct 2024 00:03:39 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2797e1c46982357d97721ee9c01ccd9a50bf390819c3e6ccc6ce7e10c311cfa`  
		Last Modified: Thu, 10 Oct 2024 00:03:39 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
