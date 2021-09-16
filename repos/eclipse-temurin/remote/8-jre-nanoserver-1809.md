## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:1547f754b963eebc6c8c2c06966900966cc1cf9e0b7131f74a7bc3d7944d51cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull eclipse-temurin@sha256:fd1dd1f27306a504c1843dd29f3747968dc5caac7525e999fd048401fbde39f3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141930090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5462080328d5f04b0f41b65163ce9b64d129de57a3b38645c9eef8feb93ff71c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 00:38:23 GMT
SHELL [cmd /s /c]
# Wed, 15 Sep 2021 16:20:33 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Wed, 15 Sep 2021 16:20:34 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Sep 2021 16:20:35 GMT
USER ContainerAdministrator
# Wed, 15 Sep 2021 16:20:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Sep 2021 16:20:46 GMT
USER ContainerUser
# Thu, 16 Sep 2021 19:15:43 GMT
COPY dir:1080d1f1dd1c0d61d0c45958055fb50fcd7599d7396f8e079867cfa7dbefbee8 in C:\openjdk-8 
# Thu, 16 Sep 2021 19:16:19 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:807d06303c39b2317729754a4c7ad6501e59c16ee464f8f671f9947774f62f72`  
		Last Modified: Wed, 15 Sep 2021 01:10:56 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5731adde04ee2252ac27813d5925fb91867aafd70d505dd0ee8c779d2f0861b0`  
		Last Modified: Wed, 15 Sep 2021 16:39:35 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ef075850bd103418d66728845f5b683d117cc72dc9975a5e22cb86e28bee97`  
		Last Modified: Wed, 15 Sep 2021 16:39:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007e224b123b02b7892d0aa9f4caf5a7c478f7d3e9792c9f21aa93237bf5da8c`  
		Last Modified: Wed, 15 Sep 2021 16:39:33 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe01989fb22d68a2c36e984344fc8dea4c076ab04d33fd563fd39da6048cb39`  
		Last Modified: Wed, 15 Sep 2021 16:39:32 GMT  
		Size: 67.1 KB (67119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987abbd4e696821e711d73f2dd27ceae2ccf2c0ae0d9478fa3422269b416f99c`  
		Last Modified: Wed, 15 Sep 2021 16:39:32 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a465fdb6f95f7b5967b411c42b2b0d4d1876cdcefff831b0520433e307842420`  
		Last Modified: Thu, 16 Sep 2021 19:23:50 GMT  
		Size: 39.1 MB (39074017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6735f57bf1bc349a0476011763da50ffc1a5236029034f6b24aff2192dc9551`  
		Last Modified: Thu, 16 Sep 2021 19:23:42 GMT  
		Size: 79.9 KB (79871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
