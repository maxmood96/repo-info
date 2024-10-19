## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:14e05f70a816a3002095353886f9437a59ec47278c68d8b61ce8005239d52420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:78c88ceafaff7552d565a4b116b8040596fe1c266c4d5d0765a11cf81f3a39a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256763226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9d274c9560f82ae076f91b421fb8acc2b4c1b722da3efc7770185c022600be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 19 Oct 2024 02:06:58 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:07:00 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Sat, 19 Oct 2024 02:07:00 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 19 Oct 2024 02:07:01 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:07:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:07:18 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:07:25 GMT
COPY dir:1819e9728b8ce1656dc0a20e5dd4c40c4149d50cae5eed15e03f81dabbaba653 in C:\openjdk-8 
# Sat, 19 Oct 2024 02:07:29 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55420a4cd104b93d5771308dc06c2b00676b241e72057656d91ca0effb5d9d0`  
		Last Modified: Sat, 19 Oct 2024 02:07:33 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca9475ba5517130ee311d2d1b4c3e8c7f0790769aaafcd928b7d7633d15179b`  
		Last Modified: Sat, 19 Oct 2024 02:07:33 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6353b39dcde6694aa340226f785986152f0acd51c3d968c6b3c74fca177886b9`  
		Last Modified: Sat, 19 Oct 2024 02:07:33 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a7b44739b12fe4f087563ceed7796ab8f40ab3b9a903c17bbd3b63879c90a3`  
		Last Modified: Sat, 19 Oct 2024 02:07:32 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149eced2c9242b4e79931866d737ca79679a2a7757b66e9244901eee3c0f72d2`  
		Last Modified: Sat, 19 Oct 2024 02:07:32 GMT  
		Size: 66.2 KB (66160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46e3f5d24d4778e47b72c81a9f3dcec620d5234990e0c49deff43cb2868bb9c`  
		Last Modified: Sat, 19 Oct 2024 02:07:32 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8604a1d5552a45b86dea08a0751d7e3c3bee017d0b5adcef84625be50565a9`  
		Last Modified: Sat, 19 Oct 2024 02:07:40 GMT  
		Size: 101.5 MB (101519083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc23a93953d955db24cb78425786f1cbd8c324ac1eca2fc19a0556201e24a22`  
		Last Modified: Sat, 19 Oct 2024 02:07:32 GMT  
		Size: 79.2 KB (79172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
