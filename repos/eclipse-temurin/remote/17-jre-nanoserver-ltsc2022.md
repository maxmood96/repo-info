## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:eb707f668e996b1b861c6aceafb05a08af9682e40a17554fd3ef3823c59c3645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull eclipse-temurin@sha256:7c7ffcddb67a767e6fb9462e9985ca1d3b789a14c87421c3bb9b0cb1d14ae4f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164111632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d99e5b63a86793d3a6a6000fc6a4a66410221d5895737040de41949b5d0c993`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Sep 2023 00:20:14 GMT
RUN Apply image 10.0.20348.1970
# Wed, 13 Sep 2023 03:28:54 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 03:31:14 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Wed, 13 Sep 2023 03:31:14 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Sep 2023 03:31:15 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 03:31:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 03:31:21 GMT
USER ContainerUser
# Wed, 13 Sep 2023 03:31:59 GMT
COPY dir:a0385e93ace109911eb3f9b447c778bc50121e83afa8a78ec38a5f32b2b463cb in C:\openjdk-17 
# Wed, 13 Sep 2023 03:32:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8f8cef0759210af9d01a2fb45d79956a2db738bbd3734b7244b17e14ad945cab`  
		Last Modified: Tue, 12 Sep 2023 18:47:39 GMT  
		Size: 120.6 MB (120567584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d67aef4c483590cefd40495efc212f13e4c62993e8036c20bb4e19bc8620508`  
		Last Modified: Wed, 13 Sep 2023 03:47:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8d421f21f43d0e258824a8327da02b26abed3d24883286056ab0d1719171dc`  
		Last Modified: Wed, 13 Sep 2023 03:48:34 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a5a6e6702b097d8587ecbb5f6abf31e9394317332fd48351918422f4ee2bb0`  
		Last Modified: Wed, 13 Sep 2023 03:48:34 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7d16f77e03c598328036fe852e884cfc812be8633393a34442fa909257b05f`  
		Last Modified: Wed, 13 Sep 2023 03:48:34 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a686e4257c37374cfc23e8b5698fc8cfe8f330e7cc6a27e9b532541367b4bba1`  
		Last Modified: Wed, 13 Sep 2023 03:48:32 GMT  
		Size: 75.6 KB (75626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec3c38f52d68a4afd9ca72b3a6ae47b3c16fa364025bce3f6d1da443518ee51`  
		Last Modified: Wed, 13 Sep 2023 03:48:32 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96327744311dfcf994347f08a3749355f66e1156eb1a77a456383f758eba29c6`  
		Last Modified: Wed, 13 Sep 2023 03:49:15 GMT  
		Size: 43.4 MB (43403276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b908b09d6fd09877e30c2718d6391ab4464081d331108455fb4dd254cf0c6c`  
		Last Modified: Wed, 13 Sep 2023 03:49:05 GMT  
		Size: 59.6 KB (59643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
