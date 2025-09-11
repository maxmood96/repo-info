## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:49c837b2748bbcb672e924e9db2d756902354ce2cefb84c51ecae9db3048e9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:51cbc4decba7a6664a1677a70e525dab09470e46b0119d59732f40d8e2ffebd9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234279025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a20030bccad348d1cebcc9ef66542422d1506117d42b0abc9e641c705c2a008`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Wed, 10 Sep 2025 22:19:17 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:19:17 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Wed, 10 Sep 2025 22:19:18 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Sep 2025 22:19:18 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:19:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:19:23 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:19:27 GMT
COPY dir:dae5853f4b111011cf1e21d00736b413be35f27636dbbe76d1c13e33a12f455a in C:\openjdk-8 
# Wed, 10 Sep 2025 22:19:30 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7201151bb0d5044d68dca1963d01e21728f6ab5eb3d653b0aa70294eb038297a`  
		Last Modified: Wed, 10 Sep 2025 22:20:41 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739acfacd71e331ce4d448b3724bddfb8c7fcf1c034e88ff7d14093bd1745bdf`  
		Last Modified: Wed, 10 Sep 2025 22:20:42 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26055e8f7a0f34823755b9d250afbb7f59d2ab329f6e2c59e9e5278b655cd283`  
		Last Modified: Wed, 10 Sep 2025 22:20:42 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3465d90ba301a0f794e4543091a1d4f686c3feabf519d87cd903610346acd54d`  
		Last Modified: Wed, 10 Sep 2025 22:20:42 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb84271bc44e65f3333f25df2798ddca3ecde6cca1704f39eaffa6ed4fb66e6`  
		Last Modified: Wed, 10 Sep 2025 22:20:42 GMT  
		Size: 78.5 KB (78478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dc990cbe29999dd4c65ad9486f36fb6625a7a2704e1e5aa689bbb668dd3eef`  
		Last Modified: Wed, 10 Sep 2025 22:20:42 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4f30e4c45380a3c14b289f222ff3fa93cde953275fbae6d2566c9ab3e2eb09`  
		Last Modified: Wed, 10 Sep 2025 22:20:48 GMT  
		Size: 40.5 MB (40548003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567cc705700dcae7bdfa26c7e7829a2fbac5e31ac4dcb091edbb584c205d792d`  
		Last Modified: Wed, 10 Sep 2025 22:20:43 GMT  
		Size: 96.3 KB (96340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
