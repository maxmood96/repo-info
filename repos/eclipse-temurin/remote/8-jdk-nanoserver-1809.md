## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:95073230438d141bb46dbd980c1a85b47ea2949153eeb7720fefa66ee2db61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull eclipse-temurin@sha256:d386f720756143a5d2a07fd832e3e3261c2ecb0826ec04287b3860cd5e0213e0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203368210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb6d84d8854fa2ff6d889e2b361418b0999b8a1e9ca9c6603e1524361b4ef9a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:33:30 GMT
SHELL [cmd /s /c]
# Tue, 11 Jan 2022 21:33:31 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Tue, 11 Jan 2022 21:33:32 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 11 Jan 2022 21:33:32 GMT
USER ContainerAdministrator
# Tue, 11 Jan 2022 21:33:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Jan 2022 21:33:49 GMT
USER ContainerUser
# Tue, 11 Jan 2022 21:34:03 GMT
COPY dir:7d20e7860b874019800a6393f3930849559cf997f64b86d2d0263d858293fa37 in C:\openjdk-8 
# Tue, 11 Jan 2022 21:34:19 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6cc5785ab09c66739c3205c3a26410f1cf4bf85c377fa81b240e754cf0659c58`  
		Last Modified: Tue, 11 Jan 2022 22:44:40 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57dbd86100c2f89c898ccb22fe49143f18ac91d265650aed86bce6ca4c440b2`  
		Last Modified: Tue, 11 Jan 2022 22:44:40 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304fb8a87b93b0c55df8e416ba8eb9e9f7c7d839f8352fba177b78db62d27961`  
		Last Modified: Tue, 11 Jan 2022 22:44:40 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3c4ec70ba8edb5640c63ab1a2a0fcb04216749b103d00170450683853ca825`  
		Last Modified: Tue, 11 Jan 2022 22:44:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af2121f00d2777a3444ebaace92855a88b75bb1709cb45ae9282cf6fbb10246`  
		Last Modified: Tue, 11 Jan 2022 22:44:38 GMT  
		Size: 68.4 KB (68365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f44e345e8a9816ad2c38838029d414a029a1d60c67879ca9a779019dcbafd4`  
		Last Modified: Tue, 11 Jan 2022 22:44:38 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1080f0cb76a1eb591d77577712588172b416a03426710aeda6f3d7ad8668fa`  
		Last Modified: Tue, 11 Jan 2022 22:46:29 GMT  
		Size: 100.2 MB (100190118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6aa9df1cb8adb70914589ea68192d14cfa80152faf9b0a337f04428b60367b`  
		Last Modified: Tue, 11 Jan 2022 22:44:38 GMT  
		Size: 89.8 KB (89777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
