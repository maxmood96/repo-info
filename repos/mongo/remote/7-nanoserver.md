## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:5005ce62d7101e108dadc158fbc96f4360c1b1248f5649f1c9c97f54ed07ae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull mongo@sha256:c124a78a969bd891d29d6d5299a3aaa6807dab8a1ee489f2b521c7a233e1af93
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.6 MB (732642848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee2fc27ec5393f3a469e7adc2eba6b640774b2ccf6baef1c2d6c4044e4401eb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 01:20:12 GMT
SHELL [cmd /S /C]
# Wed, 09 Apr 2025 01:20:13 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:20:15 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 09 Apr 2025 01:20:15 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:20:16 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 09 Apr 2025 01:20:17 GMT
ENV MONGO_VERSION=7.0.18
# Wed, 09 Apr 2025 01:20:37 GMT
COPY dir:6fcdcbf736bed5967b918eb56898f440804e5aea220d223d7002f3a8d481815b in C:\mongodb 
# Wed, 09 Apr 2025 01:20:59 GMT
RUN mongod --version
# Wed, 09 Apr 2025 01:21:00 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Apr 2025 01:21:00 GMT
EXPOSE 27017
# Wed, 09 Apr 2025 01:21:01 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9fc303073c990d29f5ce637a52014352acdeab125e356de2c1ac83c3d699cc`  
		Last Modified: Wed, 09 Apr 2025 01:21:09 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe5a38548e11b464daccd0c5a115ec8621ef5c88e8ac42ceec7fecb14bb7265`  
		Last Modified: Wed, 09 Apr 2025 01:21:09 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e22a13489513349f4f70aed331992a18e0b11f5a312f1e7fefdffb504dc40d`  
		Last Modified: Wed, 09 Apr 2025 01:21:08 GMT  
		Size: 77.2 KB (77195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de224090062925ecd3cbfe5536f26fd17e9e18d6674a6ce75d0fcbca469b9cb`  
		Last Modified: Wed, 09 Apr 2025 01:21:07 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7450bb5fa2f3a9d1f698779b919c30179bbd42a175ba3df1cffe62b488866b2`  
		Last Modified: Wed, 09 Apr 2025 01:21:07 GMT  
		Size: 275.1 KB (275143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d7fed6fb57e7299c40f990052f3d408c0b645c3a88ef04d421eb0e66e63512`  
		Last Modified: Wed, 09 Apr 2025 01:21:07 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35afbc17482f6aacc8357b5fdb085d1dd785e588873aafda713cdefe752d6b83`  
		Last Modified: Wed, 09 Apr 2025 01:21:53 GMT  
		Size: 611.4 MB (611438719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b625f0df70d5aa192fb63cb102d21f1e6b8277616783082046e3b6a2af5cc74e`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 108.2 KB (108243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4900d22d13ec369c6908c36312573a026ab3760894ecb88d44840e3a68b4c2`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ada4230d8d04166d436572f34bafc1ea98e0debec66127b845a7a414a2468e`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893f052c94b506071eb3855fd96027b3d44d7d193d0086ba913764c7f4e11edb`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.7136; amd64

```console
$ docker pull mongo@sha256:3cce01c433166a4940d7702b0d7b9d354f7ad6e94c5b946ae8f9bb927bcf0ba3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.8 MB (718784671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf2050da6adf54232902e3457132cbda16dd4f34ef92e1db62b6e76b456735d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 02:15:51 GMT
SHELL [cmd /S /C]
# Wed, 09 Apr 2025 02:15:52 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:15:55 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 09 Apr 2025 02:15:55 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:15:57 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 09 Apr 2025 02:15:58 GMT
ENV MONGO_VERSION=7.0.18
# Wed, 09 Apr 2025 02:16:21 GMT
COPY dir:6fcdcbf736bed5967b918eb56898f440804e5aea220d223d7002f3a8d481815b in C:\mongodb 
# Wed, 09 Apr 2025 02:16:37 GMT
RUN mongod --version
# Wed, 09 Apr 2025 02:16:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Apr 2025 02:16:39 GMT
EXPOSE 27017
# Wed, 09 Apr 2025 02:16:40 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73b90529f8886580d847c30ccb15d96874eae44aac88a763ac1c457b5b18a3e`  
		Last Modified: Wed, 09 Apr 2025 02:16:48 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408d4b89e57b6fbc0f237ca5240868b9c39d8e9a5eaf629df8fba6e264f7794a`  
		Last Modified: Wed, 09 Apr 2025 02:16:48 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14cc28af3752700fe0f636e639c97b46936adba19f0c47f014e1ce9276a89d0`  
		Last Modified: Wed, 09 Apr 2025 02:16:47 GMT  
		Size: 68.8 KB (68773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d58732b05db28d72f7d9b725a922ebb19eef5a16a1123613fc7478c8508572`  
		Last Modified: Wed, 09 Apr 2025 02:16:46 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779bbaf1f34b668a0605b1e5b49fc2db4109ff168b528d1962f335cf103475a8`  
		Last Modified: Wed, 09 Apr 2025 02:16:46 GMT  
		Size: 275.2 KB (275152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b26f99ef3fbe8fe554706ea347c8fd39b6f0a4a71723f089f96d600fe290e2`  
		Last Modified: Wed, 09 Apr 2025 02:16:46 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff53f08acbca7a63e51be689b163abe568887c21a9d3efbdc5e7564f7fd9fff`  
		Last Modified: Wed, 09 Apr 2025 02:17:33 GMT  
		Size: 611.4 MB (611438663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daf32fe99630c67b1a5bbe8479357559cf5c55db5a1ea54c96b10d5c2902cbc`  
		Last Modified: Wed, 09 Apr 2025 02:16:44 GMT  
		Size: 72.2 KB (72247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43392d053b407da91cdd7f42651110616806c26f1991a7b7745b2cb2434c3e9`  
		Last Modified: Wed, 09 Apr 2025 02:16:44 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678f236befae653eabe44e223bc001c01b04104b5f15c30b0b95549078588b50`  
		Last Modified: Wed, 09 Apr 2025 02:16:44 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c73fcddb9681611230d562526419b56121d9eab92089b7a56d75da0300ae54`  
		Last Modified: Wed, 09 Apr 2025 02:16:44 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
