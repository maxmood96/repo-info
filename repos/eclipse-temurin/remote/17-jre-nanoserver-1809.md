## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:9e75a3c81a7d3f1f4b34935ac4f975cc2d3ebc2a6e97a7ca7f3fefa4ec790c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull eclipse-temurin@sha256:b0bee1797fa78ee6bcecab2cb28a881cdcbcaad738c81969a459bd4e16c30355
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153130446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac235f83a2724ac4ff19559cff5cffeaf63b21c14eec97117be8eaa1122bde90`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Tue, 08 Nov 2022 19:11:41 GMT
COPY dir:20852dc87397947f41c5a6f7f30dc526aa127dbd27640e91343bc06b34d57a7f in C:\openjdk-17 
# Tue, 08 Nov 2022 19:12:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:e45eaba93d0b11220fa6e3531e8cae1c4d6ae0d772bbf4da0a4f1f5ee57e7fdc`  
		Last Modified: Tue, 08 Nov 2022 19:53:56 GMT  
		Size: 43.3 MB (43280470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa23fc48578f171a2548c53a521702946112b241b4274b88c45182ee6aa9f28`  
		Last Modified: Tue, 08 Nov 2022 19:53:47 GMT  
		Size: 3.1 MB (3050582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
