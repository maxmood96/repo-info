## `openjdk:8u292-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:4a328efc6e2c1b68000127f5b011d8831b99b2b43988e93b7bb43fb12adef4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:8u292-jre-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:a4851b939ecfd0d52ff81c7d0e547c1c15b537a2271bce953debb29f1f79c5fd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141095536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804051bc8bfde20988b7014b5e99e1f6b7f63271fd586074baac1ebaadc476d9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:53:30 GMT
SHELL [cmd /s /c]
# Wed, 14 Jul 2021 03:30:22 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Jul 2021 03:30:24 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 03:30:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Jul 2021 03:30:42 GMT
USER ContainerUser
# Wed, 14 Jul 2021 03:30:44 GMT
ENV JAVA_VERSION=8u292
# Wed, 14 Jul 2021 03:34:49 GMT
COPY dir:f730d49fd573406c508c5c18daca9d2bf81afd7c16f0b64747f54fe283bbc615 in C:\openjdk-8 
# Wed, 14 Jul 2021 03:35:06 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d8754fb12dd351c91bed29d92c703cddb135a78d8f056b6a3bf13a251c1d2d`  
		Last Modified: Wed, 14 Jul 2021 03:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3609dce65084314b4fcdbee2b4c9cac86e4ba6a2f6731228036cb6d732decda9`  
		Last Modified: Wed, 14 Jul 2021 03:58:13 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beea74f08cf2d09382b86b1680d8741d756d6136a94cbad80c4521348f4999d4`  
		Last Modified: Wed, 14 Jul 2021 03:58:13 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a284e1f3d144cb79b4c435ae2a981fcfdb8c8dc7e29dc1a4ca3fc1df81e5ff`  
		Last Modified: Wed, 14 Jul 2021 03:58:11 GMT  
		Size: 67.4 KB (67382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501cb4cf39ea8969b47e4aec6a12c620974aefe7be361eb0a17f5cd081fbeb90`  
		Last Modified: Wed, 14 Jul 2021 03:58:11 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512db6d893615b217cc11cbfe7b021240f92c66921326c18cabe10984c703b9`  
		Last Modified: Wed, 14 Jul 2021 03:58:11 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d10d4ae0ff2b488154c0b52a3079c813a47b4103bb96f36537ebce93f2c793b`  
		Last Modified: Wed, 14 Jul 2021 03:59:58 GMT  
		Size: 38.2 MB (38216860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d214268cb43e3684f45d4fce6bae854bb1fc7eb9ad12eb1cb95239b2668b28cc`  
		Last Modified: Wed, 14 Jul 2021 03:59:12 GMT  
		Size: 79.9 KB (79895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
