## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:671740aa6c34e67c49f90eff3a425603fb50a1b81597ca7c732a5a62aded729f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:9ef36eb7e5bbf6db869acec8997b54a89ebb1df73e63c41031310abecdc2bb5c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232139921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459d66c109279818beb4035bd0bce40b073c7ade1905a62bea0cb94b526397c3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:13:56 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:13:56 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 14 May 2025 21:13:57 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 May 2025 21:13:58 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:14:01 GMT
USER ContainerUser
# Wed, 14 May 2025 21:14:05 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Wed, 14 May 2025 21:14:09 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Tue, 13 May 2025 23:02:56 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587d3f7a31a00daa3d8037b092c45f12dff1c4e2211dfa1e0ad27e8cfedae988`  
		Last Modified: Wed, 14 May 2025 21:14:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528fda69d46c0888df8776440197e14f799e46aa65ab1a67a81ca44294ca195`  
		Last Modified: Wed, 14 May 2025 21:14:12 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f897a8210cf92030cd3b7298c7f5204e052d91f72b0d05620173cfa23d42ec0`  
		Last Modified: Wed, 14 May 2025 21:14:12 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f0fe9d4683283742285c4e04b8cfc1a4cf559628b076211aba0eb4ed998b9f`  
		Last Modified: Wed, 14 May 2025 21:14:11 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8904ade50e251bb53d65dd17c8e14fbb18eb85c9f72a5705ddd2ef0250f5462c`  
		Last Modified: Wed, 14 May 2025 21:14:11 GMT  
		Size: 76.0 KB (76025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdd5ba619b6852abea2b2a1e124b42fd20d0d6d0bebe7eef2f468911f451a6a`  
		Last Modified: Wed, 14 May 2025 21:14:11 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef624b7a572b9dec09c4cedb0ea6101128e81a207609c73b22694f26f648590`  
		Last Modified: Wed, 14 May 2025 21:14:14 GMT  
		Size: 40.6 MB (40554076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7670a666c46450e23e17ae52584bdaed27ab5cb21fc9cc412c6d1549b02d423`  
		Last Modified: Wed, 14 May 2025 21:14:12 GMT  
		Size: 92.5 KB (92479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
