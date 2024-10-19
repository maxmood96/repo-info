## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8ea66ddb8fffc41eda125d95ed0caf6419e0c9d60a039efb8a706fbd4b5c1ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:f55b87d4239f1d12a3ab82eac2770bd6d288a08bb949d68c8d01653f40364e69
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163941731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae769d837401a39c216344a3dc1741d146baccb256da884b1bc80ea712fe71d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Sat, 19 Oct 2024 02:17:05 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sat, 19 Oct 2024 02:17:06 GMT
ENV JAVA_HOME=C:\openjdk-11
# Sat, 19 Oct 2024 02:17:06 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:17:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:17:09 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:17:13 GMT
COPY dir:7f821e86a68e96827a3bd2a11327aaf136099e3dece9d0ac246ce6858e157232 in C:\openjdk-11 
# Sat, 19 Oct 2024 02:17:17 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6821226e6d62e56d469338dd8f2897f016275c86ace98039cbe6b33a31edd5`  
		Last Modified: Sat, 19 Oct 2024 02:17:20 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb035494bedecdcb97b2a89d281f4aef2fdc85b7fcc5669fcf83c162e142ccb`  
		Last Modified: Sat, 19 Oct 2024 02:17:20 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2749db690ad74d4cc878296dd3ea9d91b6fcc997c8529f39478787480fce4d54`  
		Last Modified: Sat, 19 Oct 2024 02:17:20 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7586062d1dd3fc7e41de399685020cc7d1d7fa97ee319adc00d9f7a3559bd357`  
		Last Modified: Sat, 19 Oct 2024 02:17:19 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6ca677463ecfbf2c43dd0d31cd855e644c814ffab3ba3566c7f54f196d6d12`  
		Last Modified: Sat, 19 Oct 2024 02:17:19 GMT  
		Size: 78.4 KB (78386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eb3bd5b0860d0fa8e77b3f7e8e7242ac465d6c8d1b2a4439a096b56a4cc7e0`  
		Last Modified: Sat, 19 Oct 2024 02:17:19 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaaec49b2a23b628a6f68ed37e1aeab124001495c31d30db0e17bc316ab4239`  
		Last Modified: Sat, 19 Oct 2024 02:17:23 GMT  
		Size: 43.2 MB (43246026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920541b9a62942d44c0944740627624c8e48623c8ad4284eac890dfbffdb5951`  
		Last Modified: Sat, 19 Oct 2024 02:17:19 GMT  
		Size: 101.1 KB (101122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:bd7e03aeee799ca74854a419c945ff9fd9fffde7c7299e2391688d441915fc49
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198482261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144ecf6c48e9f6726b593e2108dadbaaa16d8a88249ce5c10a977b500a0fe56d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 19 Oct 2024 02:07:17 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:07:19 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sat, 19 Oct 2024 02:07:20 GMT
ENV JAVA_HOME=C:\openjdk-11
# Sat, 19 Oct 2024 02:07:20 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:07:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:07:40 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:07:45 GMT
COPY dir:7f821e86a68e96827a3bd2a11327aaf136099e3dece9d0ac246ce6858e157232 in C:\openjdk-11 
# Sat, 19 Oct 2024 02:07:49 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5428821c545b951efde1337ec6ab20061b74f10a12cbd1da711ed539c959265`  
		Last Modified: Sat, 19 Oct 2024 02:07:53 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb7e22d450e3293ce49a3fef4b79a119d414305f79143a6ae24e2066157123a`  
		Last Modified: Sat, 19 Oct 2024 02:07:53 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eeab11c8eae5426cd6a258fc3858c108c5eb0dc7890e4c39c26d3dbc6a127c`  
		Last Modified: Sat, 19 Oct 2024 02:07:53 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aef71ebd2f7741afeb945825a6e5c800576fca54c97d9f0df191c61f6020ec2`  
		Last Modified: Sat, 19 Oct 2024 02:07:52 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6161f2a84e4356d9070883a5829cfb6bd3290dae682b6bc8848bfb560aa8592`  
		Last Modified: Sat, 19 Oct 2024 02:07:52 GMT  
		Size: 67.1 KB (67120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa701a790b7b46951c485a40cd369d3243f58e45939c9f05aca984c5c052270`  
		Last Modified: Sat, 19 Oct 2024 02:07:52 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e465059c9f45ad64767e83750a976010bd8289cdc23d017e7c038a8753bde7c6`  
		Last Modified: Sat, 19 Oct 2024 02:07:57 GMT  
		Size: 43.2 MB (43248375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6726cc9bb700ae7548f6af123075762185f96c0428b7ce3a7c15d620e5c9ee6`  
		Last Modified: Sat, 19 Oct 2024 02:07:52 GMT  
		Size: 67.7 KB (67705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
