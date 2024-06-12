## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:67b1306f5d2b9d54793751976837d56b0360979c7ca34e54e99a8752b76bc286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:c44f16792a5dde15990f8fa3a302305fec96f0462453f06783819a621e5b5f52
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164024591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf976e13de2a25a5894f70471f598ec000c5ea5c4af0058dceccce5c1c7f7f70`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 18:27:44 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:29:03 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 12 Jun 2024 18:29:03 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Jun 2024 18:29:04 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:29:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:29:14 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:30:03 GMT
COPY dir:b092036da9619d86aad01e40fe92454a038bf12563d3a63208d5f3f51004688a in C:\openjdk-11 
# Wed, 12 Jun 2024 18:30:15 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ae17666c85b2b00f8e5aa24951a59f0b01a1eb41704faa32e1282e0f0ef217`  
		Last Modified: Wed, 12 Jun 2024 18:52:48 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea358a99b6c4175aaf5f9486194d911138c450ffa13f45e102f1539fee9f32c6`  
		Last Modified: Wed, 12 Jun 2024 18:53:35 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67291aac9e33e31baf9decee3bafa55569a24608299e634f094e24c14a6501d3`  
		Last Modified: Wed, 12 Jun 2024 18:53:34 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f72be97270f7c9d1e5761550ec67b54b386652154067cb5f920effc045628a`  
		Last Modified: Wed, 12 Jun 2024 18:53:35 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2170e5dc67eeac86b745b8f0a1d529d966be5d40259deec56be5837417802d`  
		Last Modified: Wed, 12 Jun 2024 18:53:33 GMT  
		Size: 83.2 KB (83159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc3e14751faa5de8a8ab0d5a22999319b3b998004c05eb7df57a4e72476cb14`  
		Last Modified: Wed, 12 Jun 2024 18:53:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdd8b932eeeb86797119d04ecc12938cabd0d02a95dd3ae03e9c52b2ae62946`  
		Last Modified: Wed, 12 Jun 2024 18:54:08 GMT  
		Size: 43.4 MB (43384566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223cc452f6f8ae5be67fda220abef1a37f9bde79bdc27d9bcd5777e424f04b9c`  
		Last Modified: Wed, 12 Jun 2024 18:54:00 GMT  
		Size: 62.1 KB (62108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:c166afcccc1cb7a3bfee9cb1a391134a938ba556a2dc4fd98aeee826d7a488be
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198539904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9895e9c3b7525752e09bbd1e81bc5e0f9ed1aa1898fab33b3cd84b76c3f0abfb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 17:41:08 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 17:51:03 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 12 Jun 2024 17:51:04 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Jun 2024 17:51:04 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 17:51:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 17:51:13 GMT
USER ContainerUser
# Wed, 12 Jun 2024 17:55:54 GMT
COPY dir:b092036da9619d86aad01e40fe92454a038bf12563d3a63208d5f3f51004688a in C:\openjdk-11 
# Wed, 12 Jun 2024 17:56:04 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce076c01ab33a997d8fa4a6a49752f31455fef6df331991ad3b3736b3567321`  
		Last Modified: Wed, 12 Jun 2024 18:40:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77f119d6104e3c8342435b5ecf20e3d87fd794b0b9d432c754d791dda070c15`  
		Last Modified: Wed, 12 Jun 2024 18:43:26 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb3afe9e4bf592bc5953d90b42d691e67c1bd6e2e85f763440a46e9af8a279`  
		Last Modified: Wed, 12 Jun 2024 18:43:26 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06259e7480cb7dc7229ee508752a310efbcc003e7cce59426c878fe97b66322`  
		Last Modified: Wed, 12 Jun 2024 18:43:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8b43aaa845da9fc8d7216df2a9485bc92264455f05123c47b9c198f5359e67`  
		Last Modified: Wed, 12 Jun 2024 18:43:23 GMT  
		Size: 71.6 KB (71646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d564193114d887c543c571d7eccefb26d886f1092038aaac0050df32e66ad2ff`  
		Last Modified: Wed, 12 Jun 2024 18:43:24 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbeeebf82570c964187e303d3e2029b39011f26f43affb3df353a9593bbec485`  
		Last Modified: Wed, 12 Jun 2024 18:44:35 GMT  
		Size: 43.4 MB (43384454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516410cb85fc1e73603ccb0ba56fe2156cb6b37abf079566310e4f902c8d24ea`  
		Last Modified: Wed, 12 Jun 2024 18:44:28 GMT  
		Size: 44.8 KB (44774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
