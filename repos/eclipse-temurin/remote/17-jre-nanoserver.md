## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0cc31a6f69a1771491da13764793e3a0e96de83540268859811c17824cfe62e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2113; amd64
	-	windows version 10.0.17763.5122; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.2113; amd64

```console
$ docker pull eclipse-temurin@sha256:cf9567175018fcb58f06c46d3c3b78925a5051543732f43d88c1dd9065968fe2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164300423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2308b14d79f2ebca5cd020e9a967ff4e3408fb22e46b82b8c8c3f747648d643`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 06:09:19 GMT
RUN Apply image 10.0.20348.2113
# Thu, 16 Nov 2023 02:17:18 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 02:20:00 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Thu, 16 Nov 2023 02:20:01 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 16 Nov 2023 02:20:01 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:20:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 02:20:12 GMT
USER ContainerUser
# Thu, 16 Nov 2023 02:21:10 GMT
COPY dir:d3f692ac99669197443250e31cbc5c2f5282787fd78589cc9b6c2e91236738f4 in C:\openjdk-17 
# Thu, 16 Nov 2023 02:21:21 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:1ca4fbe907f22e883670decfa8d7f4490a79a995bb83a6c286248c21d61a62f5`  
		Last Modified: Tue, 14 Nov 2023 21:13:36 GMT  
		Size: 120.8 MB (120753560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2f0edb58e1876347bbad88c907697db94e172aa6ff4a38560ccfb68d72aa86`  
		Last Modified: Thu, 16 Nov 2023 02:37:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6af13a0bdacebb67b2c2de5f087a7c9a54fd1ddc20291a3e0113601f6fc0358`  
		Last Modified: Thu, 16 Nov 2023 02:39:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933b6deb6421eea26b734f3c395e896c14f03c96cf94415a9b9d155d3dc40aba`  
		Last Modified: Thu, 16 Nov 2023 02:39:27 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905a570baca945dfb2069746c271640bee4b949a7f068d15dabfddc23623105`  
		Last Modified: Thu, 16 Nov 2023 02:39:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0cba15fe50e81fd8c7e1ece2183869b0eb961268ba23bc1f1cd246b54d46616`  
		Last Modified: Thu, 16 Nov 2023 02:39:25 GMT  
		Size: 79.2 KB (79166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7d503f34fb8c292cc2bbcaff06c5e71f57109209f99917719b53097b237821`  
		Last Modified: Thu, 16 Nov 2023 02:39:24 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee290e0c3b16ce7f71bbee09586154f2f11fdf225d615356c7f82d01dcc1b7b`  
		Last Modified: Thu, 16 Nov 2023 02:40:03 GMT  
		Size: 43.4 MB (43387807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0327836e683c39f37a024679ce7b7038243224b79e21a4b7b89c9a0ca2dc43`  
		Last Modified: Thu, 16 Nov 2023 02:39:54 GMT  
		Size: 74.3 KB (74341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.5122; amd64

```console
$ docker pull eclipse-temurin@sha256:a6f7e4bbf23cfb43c1d3d1a257e4aba9977ae8c9c4ee3886d5b374411dee8c9c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150944131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68282f9b0c175d8e06cb50e6de83cf52f42cfb1d8e87ae6df9f6594e440fccd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 01:41:12 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 02:01:51 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Thu, 16 Nov 2023 02:01:52 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 16 Nov 2023 02:01:53 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:02:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 02:02:02 GMT
USER ContainerUser
# Thu, 16 Nov 2023 02:06:44 GMT
COPY dir:d3f692ac99669197443250e31cbc5c2f5282787fd78589cc9b6c2e91236738f4 in C:\openjdk-17 
# Thu, 16 Nov 2023 02:06:55 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5c133738aab79d4c21c47e77cb838e2d00166f5e3e2632177622f67488259`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a929d328ae624d5b0c26b2c6080f8fadda432a89348c53c823ead3ea83cb31ad`  
		Last Modified: Thu, 16 Nov 2023 02:33:28 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e523d409cba7796d6a2c3d60186d4504d38d430101cd5cdb583608c12fa3322d`  
		Last Modified: Thu, 16 Nov 2023 02:33:28 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5b00068b929a533e7e5f34941b1ff74b39efd9132278ffb636df385fdfe49e`  
		Last Modified: Thu, 16 Nov 2023 02:33:27 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69e1e253770e264976b8ecead34937818726e856ce67e8d5089d0979c58a53e`  
		Last Modified: Thu, 16 Nov 2023 02:33:26 GMT  
		Size: 68.3 KB (68316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184fd96217640a6a7136df3c143c18364cb4976aa0a3368dc067d7a12bba7a7`  
		Last Modified: Thu, 16 Nov 2023 02:33:26 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea619a6cb8614505891bc7e7a4d5773caf77dc2fbaffcd8afc4b9b714e9c1224`  
		Last Modified: Thu, 16 Nov 2023 02:34:43 GMT  
		Size: 43.4 MB (43396020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903d7447627337004bfb92e4c2d41ff5c5d446522b2fc39b5f1179ac882bf42d`  
		Last Modified: Thu, 16 Nov 2023 02:34:35 GMT  
		Size: 3.0 MB (2976592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
