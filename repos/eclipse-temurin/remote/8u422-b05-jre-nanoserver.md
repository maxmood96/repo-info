## `eclipse-temurin:8u422-b05-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:939979b33dce7ca0befe451430513e3e7bfff9cd167fb77b49ad93d4ef3ee687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:8u422-b05-jre-nanoserver` - windows version 10.0.20348.2655; amd64

```console
$ docker pull eclipse-temurin@sha256:608fc2694394f6556343a1f515b07b54a0d07a017523201bd54aa7af2696e59b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160716494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c8089aa3118f56849cb7a92f1cdd0db11ff377eaedc5d03af5c3b7fa0631e4`
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
# Tue, 13 Aug 2024 20:20:29 GMT
COPY dir:9cd76711a1e21cd053ac2280c0520b18fc7c9ba73d3efc8192b2b62cbbddbbff in C:\openjdk-8 
# Tue, 13 Aug 2024 20:20:38 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:76fd0c6a7bfac263b2e59a97c35f0e91a705abbc7c818defc4b42ac01e4cfbf0`  
		Last Modified: Tue, 13 Aug 2024 20:40:32 GMT  
		Size: 40.0 MB (40019181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbe165c448a5d1979ac9dd4f5d6d093bb116016223be2df3a1a45426c2fb1bc`  
		Last Modified: Tue, 13 Aug 2024 20:40:28 GMT  
		Size: 61.0 KB (61034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u422-b05-jre-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull eclipse-temurin@sha256:92e909988e5b71f9e720cffeeed0b741393a2de1c95f5d076b7088e0c3fc3757
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195267586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563a1e0ebafc145db68326d729499fcac2c00861ae3b16f6b056b6046fc1c341`
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
# Tue, 13 Aug 2024 19:44:19 GMT
COPY dir:9cd76711a1e21cd053ac2280c0520b18fc7c9ba73d3efc8192b2b62cbbddbbff in C:\openjdk-8 
# Tue, 13 Aug 2024 19:44:28 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:f4840fa1c379496159b54cbe1d5e8384367b33ff9efbbf0d03f0794f5e22c289`  
		Last Modified: Tue, 13 Aug 2024 20:31:06 GMT  
		Size: 40.0 MB (40019023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9128131f245900d4b58163f6a09137fbcf00d274b6c0b82b0b7b2b872b56233`  
		Last Modified: Tue, 13 Aug 2024 20:31:01 GMT  
		Size: 89.5 KB (89521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
