## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0f2fdd34d79e9e5d99246e76da5a6afda3e4e146702d941fe3d1c6a20e3b0e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.2655; amd64

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

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull eclipse-temurin@sha256:7a6e17f6335254a3e4340e9b990630f85e0810e979c136ba8df6f3f192451920
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256786027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942fd85c1d4eeedb9be4c99297d38532f3207e007ed5fbbb65cdf69625b778c1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 19:40:26 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 19:40:27 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 13 Aug 2024 19:40:28 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 13 Aug 2024 19:40:29 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 19:40:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Aug 2024 19:40:42 GMT
USER ContainerUser
# Tue, 13 Aug 2024 19:40:51 GMT
COPY dir:cf98fec7e439356342f3bf03fb67b0dac0e213296a20d5e427a9ebba9080193e in C:\openjdk-8 
# Tue, 13 Aug 2024 19:41:01 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee91db53edb9eaa638d7d926c33dc3d39a0bedf5ace2c9ff25f8c413bc3ea2c6`  
		Last Modified: Tue, 13 Aug 2024 20:30:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea35f7f090816a7fe5add0424cba285d8df77c18ec47c75e44a74608ef3a8573`  
		Last Modified: Tue, 13 Aug 2024 20:30:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65441e8750433f51ea383ecf14615ad0aeb32ac9a7a6007a17d4dad9992843f9`  
		Last Modified: Tue, 13 Aug 2024 20:30:04 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189cbb97da65c2c90ba3d40d62fa18d23f449c995650ca147be715f39f38674f`  
		Last Modified: Tue, 13 Aug 2024 20:30:02 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1772ece0bfed76416643ea51bbfb4d3151924b1f9d31132914a915edc2b125`  
		Last Modified: Tue, 13 Aug 2024 20:30:02 GMT  
		Size: 70.2 KB (70247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036c2827782fd0886f7e5607fde3d6236d41d825003869a02e2fcbe3bd66451f`  
		Last Modified: Tue, 13 Aug 2024 20:30:02 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf3347591e328ec8184510a1fdbcc3d32a22a4d869b5b9d78a4d48e8cd34d42`  
		Last Modified: Tue, 13 Aug 2024 20:30:11 GMT  
		Size: 101.5 MB (101544461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ac55a49244d850cc93ac337681b38b57f4b9d54b18a9383f2862003f4f7982`  
		Last Modified: Tue, 13 Aug 2024 20:30:02 GMT  
		Size: 82.5 KB (82524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
