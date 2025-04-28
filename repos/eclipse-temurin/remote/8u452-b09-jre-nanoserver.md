## `eclipse-temurin:8u452-b09-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a7efcc27ce18ba10dc1f2168126e324d3f87d8d7a7fc15be1e14a81411df6bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:8u452-b09-jre-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:e302ca4536e97fa0e7344f91306f8cd848893b7d0f78f8c4e45c780ce9b61bb5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230870051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d29e9d86ba9c02a043d249609ae098e746bc67b7b3b38bb223587b5f3d99bc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Mon, 28 Apr 2025 20:56:14 GMT
SHELL [cmd /s /c]
# Mon, 28 Apr 2025 20:56:15 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 28 Apr 2025 20:56:16 GMT
ENV JAVA_HOME=C:\openjdk-8
# Mon, 28 Apr 2025 20:56:18 GMT
USER ContainerAdministrator
# Mon, 28 Apr 2025 20:56:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Mon, 28 Apr 2025 20:56:23 GMT
USER ContainerUser
# Mon, 28 Apr 2025 20:56:27 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Mon, 28 Apr 2025 20:56:32 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07395187ecb0d933b1913000c3b5726dee9db0ade0ad1c64fb2326b0988fdb1`  
		Last Modified: Mon, 28 Apr 2025 20:56:35 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a898e392ece2fc555edf73941d59d9965b11ed95d9b8e32b66c6300928f539`  
		Last Modified: Mon, 28 Apr 2025 20:56:35 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a848d6605d20e938cd97120ac6fb0ea4c0162d390cf8430a681d1e18c32352`  
		Last Modified: Mon, 28 Apr 2025 20:56:35 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b2735aac0c5648946946a1e97e29df9b472367d130044fae39a7f8eeeb2901`  
		Last Modified: Mon, 28 Apr 2025 20:56:34 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b9f4f8bd79cc59d39487508ac2e9cd027bb809f2d65c99b12d4732121c10df`  
		Last Modified: Mon, 28 Apr 2025 20:56:34 GMT  
		Size: 76.2 KB (76213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2299d4e12ae5f7db365a3fd90213eeaecbc1fdff776da5070030c2ff0badd77`  
		Last Modified: Mon, 28 Apr 2025 20:56:34 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30efc06610947c1b434602b573c537e0a97399dc1dfe6d1682f9e994bf062db5`  
		Last Modified: Mon, 28 Apr 2025 20:56:38 GMT  
		Size: 40.6 MB (40553994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3820c24f7b91a10dcc8ab31e6478b8030603331c70582d054f47174cb9252f8`  
		Last Modified: Mon, 28 Apr 2025 20:56:34 GMT  
		Size: 92.5 KB (92526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u452-b09-jre-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:0c1538ce5b145cba9988690465cef23d4f82d5a9090faa373a62d2b4a2bb18d4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163279916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c88835e97a9bb1de307afb58f2fe5e1158007d68ec937822ff094161acb868`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Mon, 28 Apr 2025 21:00:13 GMT
SHELL [cmd /s /c]
# Mon, 28 Apr 2025 21:00:13 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 28 Apr 2025 21:00:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Mon, 28 Apr 2025 21:00:15 GMT
USER ContainerAdministrator
# Mon, 28 Apr 2025 21:00:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Mon, 28 Apr 2025 21:00:39 GMT
USER ContainerUser
# Mon, 28 Apr 2025 21:00:42 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Mon, 28 Apr 2025 21:00:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f64b6eb4a92f1246dad93a3c5b2ac90c54292500eaf3e947a262d79b15b524c`  
		Last Modified: Mon, 28 Apr 2025 21:00:50 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee035c8d011dfcede2d03d0c5081983419d614810ad1f8ce8ec1cd9e9b38ddd9`  
		Last Modified: Mon, 28 Apr 2025 21:00:50 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90abd3ce4e4cea7d993f8990b5740108428cfb7fb29db1260e7a700ef0ea9e5d`  
		Last Modified: Mon, 28 Apr 2025 21:00:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981d8c6d2c158fa1ef7e6b9749162e876026d117bcd4d92ab6942b4dd3f1204d`  
		Last Modified: Mon, 28 Apr 2025 21:00:49 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee12339e58527771d6d3bf7ee0ff454328e149028caad420b5c961e010ab4c6`  
		Last Modified: Mon, 28 Apr 2025 21:00:49 GMT  
		Size: 88.8 KB (88755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618da349be872c00c690a63682ccdb728d1872d2a330eecc880e044601737e25`  
		Last Modified: Mon, 28 Apr 2025 21:00:49 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0955a7f11aaf68d0f91af9d27f22baac006dfc8a1f174902984eef71b6b48501`  
		Last Modified: Mon, 28 Apr 2025 21:00:53 GMT  
		Size: 40.6 MB (40553112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffc1a7bd90288e4d032e6af82f0dd8d95fa0f51d118076988025c91644514be`  
		Last Modified: Mon, 28 Apr 2025 21:00:49 GMT  
		Size: 93.7 KB (93736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
