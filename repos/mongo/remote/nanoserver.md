## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:7f63db7c342fe2f421f35695cc4c7786d132845ea60ddd28ef07ca47277aa8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `mongo:nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull mongo@sha256:54cbc1f190bf10be351b8c8de8b8a0deb139f43dd928ebd88352de2673da0a7b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **728.7 MB (728653231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6805472f4072f70b9640dec1270abd93be74eee539009d40cb6df5204a605591`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 18:06:42 GMT
SHELL [cmd /S /C]
# Wed, 10 Jul 2024 18:06:42 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 18:06:45 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Jul 2024 18:06:45 GMT
USER ContainerUser
# Wed, 10 Jul 2024 18:06:46 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 10 Jul 2024 18:06:47 GMT
ENV MONGO_VERSION=7.0.12
# Wed, 10 Jul 2024 18:07:13 GMT
COPY dir:f0b5fa50aabc110faf03295e6346b9d39d589dd155d9a16877c392688d63cd36 in C:\mongodb 
# Wed, 10 Jul 2024 18:07:27 GMT
RUN mongod --version
# Wed, 10 Jul 2024 18:07:28 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jul 2024 18:07:29 GMT
EXPOSE 27017
# Wed, 10 Jul 2024 18:07:30 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f704acaec58d1e6229330140e5e5b1398ee7fe1871c88a59a6db18af9781303`  
		Last Modified: Wed, 10 Jul 2024 18:07:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234f00af74ff846e1f3a743fc93a1f718bcb3e010457f9be92bc0b2eff853f6a`  
		Last Modified: Wed, 10 Jul 2024 18:07:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3d023b67279b1b4a1bef31cec1eacdd9aa129158b86791faf8d64dd1de1f8c`  
		Last Modified: Wed, 10 Jul 2024 18:07:36 GMT  
		Size: 78.4 KB (78379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56904e2e89a20ea0dc9f2d5a4135a8cbec1fa011ce3f8259a29b2e2e6190aa08`  
		Last Modified: Wed, 10 Jul 2024 18:07:36 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5bc5ed920ce0e53834015afbd6da45d4207683f4311bc352e307415507e321`  
		Last Modified: Wed, 10 Jul 2024 18:07:36 GMT  
		Size: 275.2 KB (275159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379db936979245d472dfbd6c207714e9437ecf148be33c5b11c0975d599c47d1`  
		Last Modified: Wed, 10 Jul 2024 18:07:35 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7b24f4f89b281f7a23948de6efd4eb60ba12a2ed64c5aff792cfe1c6cb3fd1`  
		Last Modified: Wed, 10 Jul 2024 18:08:22 GMT  
		Size: 607.7 MB (607714596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d646c5e6244573b07b22785e5dbe045ed5f780dc1bdce228375b9065d702ed15`  
		Last Modified: Wed, 10 Jul 2024 18:07:34 GMT  
		Size: 87.3 KB (87337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4c219302c5e74a916f67a827ed46691ef95699eedc32d7f913dd747ccad514`  
		Last Modified: Wed, 10 Jul 2024 18:07:34 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abda12e2dcfb71e30ce7789c473b680723a23ce384928ae2705019a9aecd04a7`  
		Last Modified: Wed, 10 Jul 2024 18:07:34 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27ec407cadfff4c0716f48d826c49e27f1b19d6e195086c1856e2827fd42d9e`  
		Last Modified: Wed, 10 Jul 2024 18:07:34 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull mongo@sha256:7f1a1c3d300ac7d6f4fbdcf0914fce0828811aeaf5c294d33df8f15aff0cb4ad
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.4 MB (764354646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b21f09c241b018e2d482232d7abcc316bda585748c072585ecb597571b6aff`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 18:13:40 GMT
SHELL [cmd /S /C]
# Wed, 10 Jul 2024 18:13:42 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 18:13:44 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Jul 2024 18:13:45 GMT
USER ContainerUser
# Wed, 10 Jul 2024 18:13:46 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 10 Jul 2024 18:13:47 GMT
ENV MONGO_VERSION=7.0.12
# Wed, 10 Jul 2024 18:14:23 GMT
COPY dir:f0b5fa50aabc110faf03295e6346b9d39d589dd155d9a16877c392688d63cd36 in C:\mongodb 
# Wed, 10 Jul 2024 18:14:32 GMT
RUN mongod --version
# Wed, 10 Jul 2024 18:14:33 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jul 2024 18:14:33 GMT
EXPOSE 27017
# Wed, 10 Jul 2024 18:14:34 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f96ad17fbb0d3d88270e5cb0a9e3acb3540fb291d627b27c49880bf87a8260`  
		Last Modified: Wed, 10 Jul 2024 18:14:42 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0df23307648e0a087838505a19252408726bd1007a60dd9b4c9315ab81a411e`  
		Last Modified: Wed, 10 Jul 2024 18:14:41 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32576aa665c526e534c2e76a0fd3fd0b98b27afe58300fe64811294636ff3e07`  
		Last Modified: Wed, 10 Jul 2024 18:14:40 GMT  
		Size: 71.0 KB (71039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83046fa93931a627939d300f18876689e96292e0cb052d5e68ccb60304df5871`  
		Last Modified: Wed, 10 Jul 2024 18:14:40 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffa29c3732f12a474a560289d91e5e941180ec0cfc78509b68ac5e3a3fd10cf`  
		Last Modified: Wed, 10 Jul 2024 18:14:40 GMT  
		Size: 275.2 KB (275161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1addf7a08ff4fc19e7a331e43dbcb7f02f630ff11dfd0ceccccf21b3788a1e02`  
		Last Modified: Wed, 10 Jul 2024 18:14:39 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b9c4f24cb37202a3e0db5542e03d857906277d6f168dd96cccfe0a405d6f9`  
		Last Modified: Wed, 10 Jul 2024 18:15:26 GMT  
		Size: 607.7 MB (607714783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c0eeeb3daa6607f8cb679eaba99283a928869b8c6c84fef22c62c1d2bd5965`  
		Last Modified: Wed, 10 Jul 2024 18:14:38 GMT  
		Size: 1.2 MB (1204986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f3e951bc60aaf1361c60cda39b0100445225597ea28a52ba5d263663795c9`  
		Last Modified: Wed, 10 Jul 2024 18:14:38 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68230b26a0fb06085af27a5fe04fa5a9f230553214dda0ea72d0be8dae71c0b0`  
		Last Modified: Wed, 10 Jul 2024 18:14:38 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c270414d880d0d98e47309801a83fd54c13802501988e429ca4c9f04353684e`  
		Last Modified: Wed, 10 Jul 2024 18:14:38 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
