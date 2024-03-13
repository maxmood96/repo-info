## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ee221cf147a6490fc7518313fe6e49296b9cbfcd8f9256f1d377f81c8394148d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull eclipse-temurin@sha256:49994c8b30696e1e99e82ce6cab33837a746f8ee9c3c9d111ff31761c8cdf998
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222556325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b30bb9f2d13dc73897ba20b177429142978ac3df2b1618a8c1c067770e2a0d0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 01:20:55 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 01:20:55 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 13 Mar 2024 01:20:56 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Mar 2024 01:20:57 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 01:21:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 01:21:11 GMT
USER ContainerUser
# Wed, 13 Mar 2024 01:21:22 GMT
COPY dir:9ab35a15e19e8247451d444f7de2a75fe407ec1749c1b49082dcaaef6c80dafd in C:\openjdk-8 
# Wed, 13 Mar 2024 01:21:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e98336f720b829e374bd1d59306210d3700861b11d3df51506afbc0b50d039`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c079b182eda7b2ab08c47e780f59a7b77e54541a35de305d05927577035b30b9`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6059e0fbeac8935bc15cc89e2b57e005314533c61cf3d4276b5e731fd46fef35`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8070e272015e9632bdda4cd151f601deeeb4345fcf61701d5133689cca3ed6`  
		Last Modified: Wed, 13 Mar 2024 01:40:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21dba345c47f39abd739524299d8d68413c670c39bccce29ba922fd4e548e735`  
		Last Modified: Wed, 13 Mar 2024 01:40:24 GMT  
		Size: 84.0 KB (83968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a06064b35b70fc8c4f626eb883a0d291ba26423f241de3f0ddb0f7cd83641`  
		Last Modified: Wed, 13 Mar 2024 01:40:24 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14e6dca7370deac3b79b79862161979dd348d700cb03604e784ce36c3282de`  
		Last Modified: Wed, 13 Mar 2024 01:40:36 GMT  
		Size: 101.7 MB (101701591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427515eee0dd740df8b15a89d7ef2ff9d045bedbea8778e7860468e7847c3064`  
		Last Modified: Wed, 13 Mar 2024 01:40:24 GMT  
		Size: 62.2 KB (62246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
