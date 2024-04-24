## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7c5b65b94bf2b0ed86c90991a899e6b0bf969901b131532adcdb5d4bf8af37fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:472eaabca451f40e11e154954a35e363e0aa7763f80f436d40b90866ac2f05c7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222851433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59645ed51412bffc91dff8d24bda4d4cc7ad4d67a41a416da91e5b3aa3da62f8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:22:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 24 Apr 2024 19:22:38 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 24 Apr 2024 19:22:39 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:22:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:22:55 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:23:06 GMT
COPY dir:5498972beafb1de3e4749bc87b064f8ce9cec472aae9e7d0f4643a99f48638da in C:\openjdk-8 
# Wed, 24 Apr 2024 19:23:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a568162a8db2139c9b7f50bdca7e6de2f6e46f3a23196ccf7b33d019ad6c3f4`  
		Last Modified: Wed, 24 Apr 2024 19:46:08 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76150342796de52322a78b1675aa420817cbf16aa69b853f3213c97193064da1`  
		Last Modified: Wed, 24 Apr 2024 19:46:08 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d61c15b18ab0fae7ccb0fec0d9464105deb40fe2b2e29d96c6d93975524297`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792f549969d948ee4d8765477e3d71b4a2d4fa9c0c89daec775697ad31d12ad0`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 86.3 KB (86274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c5d1ba740a169c8c5fabb77a7268e210555e1c13d639548d947228a4f7d950`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f7f65d1806775b9c8297585522ec3b7b170e05b4b3be6937d2db568803d73a`  
		Last Modified: Wed, 24 Apr 2024 19:46:17 GMT  
		Size: 101.7 MB (101705268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb7440a247a985251799b5315f62efd778bab9d5492f8b0b99e9eed88dbc7e5`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 61.0 KB (60973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
