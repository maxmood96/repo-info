## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:f42b21a85bcf7a5895c7890cf23ba806136696c4f8d0f8a07617a59e844d0a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull eclipse-temurin@sha256:1ca044f61567275c46eb95ded247e1e1c30d102509b630ffa5a50d773f3c4cab
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222251267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fd3001f08085e0cf98fec240fd50ad51cba2c2858f3faa77d2047b32ea8fdc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 Aug 2024 19:28:00 GMT
RUN Apply image 10.0.20348.2655
# Tue, 13 Aug 2024 20:19:48 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 20:19:48 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 13 Aug 2024 20:19:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 13 Aug 2024 20:19:50 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 20:19:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Aug 2024 20:20:00 GMT
USER ContainerUser
# Tue, 13 Aug 2024 20:20:08 GMT
COPY dir:cf98fec7e439356342f3bf03fb67b0dac0e213296a20d5e427a9ebba9080193e in C:\openjdk-8 
# Tue, 13 Aug 2024 20:20:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:695cae91f2de8dadf81c8b3a95f4942533ef064a72ad8fa7843cca84a839bfba`  
		Last Modified: Tue, 13 Aug 2024 20:02:51 GMT  
		Size: 120.6 MB (120554921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8146ec246b230c09f8b628d688c831ad1269b9cef24c5c95a8d1eb2f76b89bdc`  
		Last Modified: Tue, 13 Aug 2024 20:40:03 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba656c28ab91efb82bbb828a2aad2ff2d98e72161a8b2060102084abfbfe811`  
		Last Modified: Tue, 13 Aug 2024 20:40:03 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd0395ebdedd918faa1b43b6cea4bdd67ab42140f459d549f16bf096cc8b804`  
		Last Modified: Tue, 13 Aug 2024 20:40:03 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fe2a0d1fd17d31237872ba3ac85755676c48fe10486f098073779910d10af6`  
		Last Modified: Tue, 13 Aug 2024 20:40:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3889abbe2bcd38b2562775defce30cd2a4ad6527fda1fc90ec98104b57d9809`  
		Last Modified: Tue, 13 Aug 2024 20:40:01 GMT  
		Size: 76.1 KB (76071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfe5091f204efb7c32d042d39828cd79675e46a235990432e96306f1b53947a`  
		Last Modified: Tue, 13 Aug 2024 20:40:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97de5b8bde4b8620ece83f9b35e6a8d6681b46f470c907a1629c894bd02cd86`  
		Last Modified: Tue, 13 Aug 2024 20:40:10 GMT  
		Size: 101.6 MB (101554029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a72f95e924a4fb759e23a2bfb18a220a6fcdbde1126bb1fc9e43f7c9bf6c652`  
		Last Modified: Tue, 13 Aug 2024 20:40:01 GMT  
		Size: 61.0 KB (60959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
