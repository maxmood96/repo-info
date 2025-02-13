## `mongo:8-nanoserver`

```console
$ docker pull mongo@sha256:40d1b47fde28bbef28b7d45f1ccd9e9874d33f1ef36933fa771afb747189a4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `mongo:8-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull mongo@sha256:8f5b16cd1ac0f0417ad8d926cc0723d9155f0dac22d9f0396c36b3c5973fa891
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **888.7 MB (888721409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1843120c170edc56bb4cb68d58c1ab64e7a3befbbe88b867a185aceed1f6401d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:06:28 GMT
SHELL [cmd /S /C]
# Wed, 15 Jan 2025 18:06:29 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:06:32 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 Jan 2025 18:06:33 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:06:34 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 15 Jan 2025 18:06:34 GMT
ENV MONGO_VERSION=8.0.4
# Wed, 15 Jan 2025 18:07:03 GMT
COPY dir:0009924507cd67bb774ae279cf5a575db39e491af9c3c9f55c5a3622f7b63de5 in C:\mongodb 
# Wed, 15 Jan 2025 18:07:29 GMT
RUN mongod --version
# Wed, 15 Jan 2025 18:07:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jan 2025 18:07:30 GMT
EXPOSE 27017
# Wed, 15 Jan 2025 18:07:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Wed, 15 Jan 2025 01:24:28 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d5827d687bfdd928cb53fd71ea7a8c8269c8275576cbf8eee52463f456778b`  
		Last Modified: Thu, 06 Feb 2025 07:13:07 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e37cc6dd3cba02be9dda2081aec27cfd08676556d5131bfa542bb8a4443cc66`  
		Last Modified: Thu, 06 Feb 2025 07:13:08 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321ca10b8ee0b0bb3281bb3aa96ea8311c7b2844ba4fe7360f6be37ec3bcac15`  
		Last Modified: Thu, 06 Feb 2025 07:13:07 GMT  
		Size: 78.6 KB (78568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afc4f1c8eb30b1d6f1d8fcc295532faa76c42ddfa56e77e30f893afc231cb9e`  
		Last Modified: Wed, 05 Feb 2025 06:13:39 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2414160a98cba235c1f10174925f5d113f5b43bf3fdd50cc55046b9350929a2e`  
		Last Modified: Thu, 06 Feb 2025 07:13:08 GMT  
		Size: 275.2 KB (275159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664ec6e6755ef7b1827356fbb311de08241665f5aa2fa10c5e1a1361c89d41f6`  
		Last Modified: Tue, 04 Feb 2025 04:05:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afb0ebc7e4c8a1c940acf9395d6bed19fc74e7e5edee27a74f02eda4b3689b4`  
		Last Modified: Thu, 06 Feb 2025 07:13:25 GMT  
		Size: 767.6 MB (767598358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eef94e41edda4d9d7c8cd56528e88807646af66632659303d5c491a8e72beae`  
		Last Modified: Thu, 06 Feb 2025 07:13:08 GMT  
		Size: 100.5 KB (100510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c8ca263f8eae706447700d08732f4ac72b7efc068798a966c94c1f77b35d98`  
		Last Modified: Wed, 05 Feb 2025 06:13:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0cc21ab11ca390c2c8d2406aa8b700f4db8199b3ab484e8a39ad6d55f76580`  
		Last Modified: Thu, 06 Feb 2025 07:13:08 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda1a15340546dfbfb34eae646ab442928db1299f44b7ae33cc9e731a8fc19ad`  
		Last Modified: Thu, 06 Feb 2025 07:13:09 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:8-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull mongo@sha256:4c6fadec87dd5e19a044a62fa132481a33d2cdbcb71207d238f226d01a2c2be2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.3 MB (923317103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90367d7835f322e3d32755eace44d311ad600e31acb20e11644469a89255af6c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:09:41 GMT
SHELL [cmd /S /C]
# Wed, 15 Jan 2025 18:09:43 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:09:45 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 Jan 2025 18:09:45 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:09:47 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 15 Jan 2025 18:09:48 GMT
ENV MONGO_VERSION=8.0.4
# Wed, 15 Jan 2025 18:10:14 GMT
COPY dir:0009924507cd67bb774ae279cf5a575db39e491af9c3c9f55c5a3622f7b63de5 in C:\mongodb 
# Wed, 15 Jan 2025 18:10:37 GMT
RUN mongod --version
# Wed, 15 Jan 2025 18:10:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jan 2025 18:10:38 GMT
EXPOSE 27017
# Wed, 15 Jan 2025 18:10:39 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Wed, 15 Jan 2025 07:23:16 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184e7c889c7ef1af69d399a9f610baa790f14c383aabc212884bfe8bed9101b6`  
		Last Modified: Wed, 15 Jan 2025 18:10:46 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1510c7568d3262c0896ac36dd55c122098be270f4d63cd5971d31ed082f0cb1`  
		Last Modified: Wed, 15 Jan 2025 18:10:46 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03bd9164a0c1aa137a30cf524c7ea5b99d08afe7baf37b06a0c8b5ae79331f`  
		Last Modified: Wed, 15 Jan 2025 18:10:45 GMT  
		Size: 90.1 KB (90099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68bfcc8d8fea5468de750c658949aa5cd44ccdb7cd8c936234e15ce9ef47ac8`  
		Last Modified: Wed, 15 Jan 2025 18:10:44 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a2d1d075fc4999e9a817e757578f056f17c93369de0bd33c483e35731e5a62`  
		Last Modified: Wed, 15 Jan 2025 18:10:45 GMT  
		Size: 275.2 KB (275218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4455ad1cc933857ad67552ceb15cac89c7284b4185d2430b776b67054312850`  
		Last Modified: Wed, 15 Jan 2025 18:10:44 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db2f84c776165ddedd6de8b059999b6a1f6046361bd540206134943a24d3d31`  
		Last Modified: Wed, 15 Jan 2025 18:11:42 GMT  
		Size: 767.6 MB (767598470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe07fb1c05b8326bfe62b42b1460d25968a397f3e39f8531d551f5649fd5e61`  
		Last Modified: Wed, 15 Jan 2025 18:10:43 GMT  
		Size: 78.1 KB (78135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d48354c99a9155e02935ca56635bedc1ed4c938a1e3b92bd70e4d7a763429`  
		Last Modified: Wed, 15 Jan 2025 18:10:43 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0664021524dd046855a38b6cbc8efd38b980f1b6396dc380c1ea456968ff5949`  
		Last Modified: Wed, 15 Jan 2025 18:10:43 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5821b9b3ff1d09ac5f111aa67e7827b4b6f1708941b0609ef732011a07b3eb97`  
		Last Modified: Wed, 15 Jan 2025 18:10:43 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
