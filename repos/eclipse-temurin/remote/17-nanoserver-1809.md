## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e62f0642ca3aa4519e4b53837dc8c4cdc2120ca004a82b7e4a67c17744bc602c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull eclipse-temurin@sha256:84da831330ec6ec917140a87878b984edab01d10807223a3207d7031c20abd3c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295893361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1dde02cb612ae9e8fca4681b293a4d8512e9cd74362ad714bc2800313526d9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Tue, 08 Nov 2022 18:36:25 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 19:05:04 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Tue, 08 Nov 2022 19:05:05 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 08 Nov 2022 19:05:06 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 19:05:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 19:05:19 GMT
USER ContainerUser
# Tue, 08 Nov 2022 19:05:36 GMT
COPY dir:a12ba5a18c812bc88dc6c1e12f0d0bdbacab70db88697cd6bad273d4570ac4fb in C:\openjdk-17 
# Tue, 08 Nov 2022 19:06:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Nov 2022 19:06:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e8f4bb4b79b67857c1e4ac5c66026fd5ff5badbde5a8b59b11251b02699586`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728b19a01e1b46a120b42a3b2a7535421722e52ce56376a673ad470d61c74f6d`  
		Last Modified: Tue, 08 Nov 2022 19:52:25 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ec0e424a6fac75aa67218f7a281c11d03d0d64b9f50922427f6441d2b82c95`  
		Last Modified: Tue, 08 Nov 2022 19:52:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed85d131d2f653cf456952c38b38099abd8089e91bebc9bb827f08e2cdba1c9`  
		Last Modified: Tue, 08 Nov 2022 19:52:25 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e76cd29e9e7987d476226ff8e87682ec0bc20ac4ec608747c2f45705846a94c`  
		Last Modified: Tue, 08 Nov 2022 19:52:22 GMT  
		Size: 70.2 KB (70186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fe828122921910e65a8a25576dcd55c815908b58dea415dc13bc738c8a0523`  
		Last Modified: Tue, 08 Nov 2022 19:52:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7693e5e63a2d8c8efc49e9941ed4fc3a3187a8e73712a85b58586e9e7c2b102b`  
		Last Modified: Tue, 08 Nov 2022 19:52:44 GMT  
		Size: 185.4 MB (185427863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d39917ef6a3f4586f0507b905f3d4f482327ed469defe39544927149e272927`  
		Last Modified: Tue, 08 Nov 2022 19:52:23 GMT  
		Size: 3.7 MB (3664936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afd4aec47b01ac7c25db8fb9fe7a6e1010c905bc2f4999ea8d7f783a43201ed`  
		Last Modified: Tue, 08 Nov 2022 19:52:22 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
