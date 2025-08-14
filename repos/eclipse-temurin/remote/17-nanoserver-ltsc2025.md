## `eclipse-temurin:17-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1c45c9ccd64d6b85475e1dac16500e0dd5810134523d927b51ca8533378c434a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `eclipse-temurin:17-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:317dc242fbb26d781f3d655bf8d7502b07fc6cac34e75af6d2686c43a0c8fc72
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 MB (381018724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65321453f4c940dbf004b73c3a482b924b258447bcb4e08be0521f90ef6fd23`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:50:16 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:17 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 12 Aug 2025 20:50:17 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 12 Aug 2025 20:50:17 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:50:20 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:25 GMT
COPY dir:9871f8b851cdb90a4def8faeecdb142e7e99c62806f58a649ca6456cf4e2326c in C:\openjdk-17 
# Tue, 12 Aug 2025 20:50:28 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 12 Aug 2025 20:50:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094cf1370fb6228ccb6b6d949d17ac58b175ee2974a93ce58f8ebab6ecb34832`  
		Last Modified: Tue, 12 Aug 2025 21:15:08 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569ed37a818fd21a73453da7c97962b27de1570b57b3c3a42c9ce831451c21db`  
		Last Modified: Tue, 12 Aug 2025 21:15:07 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64c01e0bd2ab8842fc0e7c77af0d317ddde8c92a5d8796fda183d1d8cb72636`  
		Last Modified: Tue, 12 Aug 2025 21:15:07 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e42cb1c129059477524560815a4ba96faa3acad8df5cb65953107e4a5a41101`  
		Last Modified: Tue, 12 Aug 2025 21:15:07 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8064d33eeb37129da8b29a670aa4d5346fcd868cf9933ec42ae87c841b5ae400`  
		Last Modified: Tue, 12 Aug 2025 21:15:08 GMT  
		Size: 75.5 KB (75521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc5d0c397bf675ccf8dfbce52f4ba42af5628935ef6bb9b72723ea65681a36c`  
		Last Modified: Tue, 12 Aug 2025 21:15:08 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13eee367378f3bc5287c99b19ab203adaacb2021400080dd07e8b19c23abc057`  
		Last Modified: Tue, 12 Aug 2025 21:15:28 GMT  
		Size: 187.4 MB (187354024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172646237e56ac47f2c7bcc3d1eda20d1090b3da6082be4c4a8a0f3b0f62782e`  
		Last Modified: Tue, 12 Aug 2025 21:15:08 GMT  
		Size: 113.3 KB (113306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6398ea8b11a5afa91ab8a985155f6a68dc23b97bdd30ba843ae87cc8c16710ab`  
		Last Modified: Tue, 12 Aug 2025 21:15:08 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
