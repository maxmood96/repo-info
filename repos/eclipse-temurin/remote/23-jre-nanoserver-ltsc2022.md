## `eclipse-temurin:23-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:56faec0f2f34c3755a900187fec4630d166cd36b7170eb046fa2416189bf03de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:23-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:f9bc72c3206885026e0d107037aa4f3e42518fb0561e862cfc225d6b9ad296e7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169852635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3909b846526d4ac86336bfeee63782bc3f912fbfa2b95a7c9cf69d39f9422493`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Fri, 31 Jan 2025 02:11:35 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:35 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 02:11:36 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 31 Jan 2025 02:11:36 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:11:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:11:55 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:11:58 GMT
COPY dir:f0b8f3d1970d52810d59047a7e1dfff98787b37140cc4aafc37fc86b09fa8be8 in C:\openjdk-23 
# Fri, 31 Jan 2025 02:12:04 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0461d7645946acc97b5b237b4b46890470321be3465bda44a0995c1ac05f075c`  
		Last Modified: Fri, 31 Jan 2025 02:12:07 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097ab02939cc933c25553324bbd4c0ae6bf3706fc63a57fe1a6824c88b9e2fad`  
		Last Modified: Fri, 31 Jan 2025 02:12:07 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881849a4af99da8a51a84653eee2a5ddc55928e4a5eab2b712969d50c6cdbd95`  
		Last Modified: Fri, 31 Jan 2025 02:12:07 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cec4b400b6176468645e0ed479ee1215072fb4fa06d4ca855916a84018d547`  
		Last Modified: Fri, 31 Jan 2025 02:12:06 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cc46d028d5b03b1eb039849620933b5e1d41ebee9a8b2a80e506895aca26c7`  
		Last Modified: Fri, 31 Jan 2025 02:12:06 GMT  
		Size: 97.6 KB (97563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2bb0cb5f00a7572ce98e9efd28474bbc75e07bb30cf77de9213e352bdb24b7`  
		Last Modified: Fri, 31 Jan 2025 02:12:06 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab146dac4ca95369c446cd87816467e88f8a3bc874a238e4fb68afa66d28fc4`  
		Last Modified: Fri, 31 Jan 2025 02:12:11 GMT  
		Size: 49.0 MB (48979971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff1191d08dcc26a049e3c31f992d564c9102d6ea3b841ed56e69bbc9df2eef8`  
		Last Modified: Fri, 31 Jan 2025 02:12:06 GMT  
		Size: 108.4 KB (108362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
