## `eclipse-temurin:26-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:eb3a74c0a8a6a14b3c3743f490045228b55840494c6d034cf8e7a4a7aff0b9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `eclipse-temurin:26-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:d5fad73a113f1aefe03710e7ddc4d50a0edd7113c9670437f5516c5232fb979d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257105083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd941192873746157ba9be26d9d1afa8bbdf5f3144d0b46afa401f2c4ae4615b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:21:32 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:21:33 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 09 Jun 2026 23:21:33 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 09 Jun 2026 23:21:34 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:21:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:21:37 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:21:52 GMT
COPY dir:1edec5af9445e163af5cd51feafb262ed7498368c1981b477e0c90d82a11e11a in C:\openjdk-26 
# Tue, 09 Jun 2026 23:21:57 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed0e4fd17aac5ffa49a256459fd022f7b3c3fd590a21fb7a72504812e63db3b`  
		Last Modified: Tue, 09 Jun 2026 23:22:02 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3fa84656ac09684dca95052d6d4076e48d21dde962593f9bc95f9823165208`  
		Last Modified: Tue, 09 Jun 2026 23:22:03 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f11c94b973cac849aa701d2d9e32f454c94e4f5a7f28dbafb2f42befbceb04`  
		Last Modified: Tue, 09 Jun 2026 23:22:02 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c1f9c2ee5245e94bc318fcd7862e797c86a4f1bef154c1e36273f2ba6c9663`  
		Last Modified: Tue, 09 Jun 2026 23:22:01 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520fdeeb076667c72281d310d9ccbe0038c45fdd9fd59dbb5f4362b6ea6e896`  
		Last Modified: Tue, 09 Jun 2026 23:22:01 GMT  
		Size: 72.5 KB (72533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a68120745bb0b3bc77d58a511987a86afe647ecb18c608bb0c730c1c16a476`  
		Last Modified: Tue, 09 Jun 2026 23:22:00 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2d7d91ad46ab34bdc5a4ae8da934a4396834805e9e02698d98cf0c93640c0a`  
		Last Modified: Tue, 09 Jun 2026 23:22:09 GMT  
		Size: 60.2 MB (60225741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767f99bf8f7434d5adebfe7b98c83a9261a43d5a2ae24ebd9023953a6672c900`  
		Last Modified: Tue, 09 Jun 2026 23:22:01 GMT  
		Size: 133.5 KB (133512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
