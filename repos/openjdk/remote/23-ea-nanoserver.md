## `openjdk:23-ea-nanoserver`

```console
$ docker pull openjdk@sha256:9741571c555fb2e2d72e4fdf30ebf4b0dde2657568ef1b568c6599decc858ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:23-ea-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:53f1d6ad2aaf3d3686d671e25102d726af620df807a7aa15007cd18ea7efa82f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307340126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3b57ead19c256c90cc599c65f00cc3a706587123dfc00c273405600d4e3c3a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Sat, 09 Mar 2024 02:48:38 GMT
SHELL [cmd /s /c]
# Sat, 09 Mar 2024 02:48:38 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 09 Mar 2024 02:48:39 GMT
USER ContainerAdministrator
# Sat, 09 Mar 2024 02:48:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 09 Mar 2024 02:48:48 GMT
USER ContainerUser
# Sat, 09 Mar 2024 02:48:48 GMT
ENV JAVA_VERSION=23-ea+13
# Sat, 09 Mar 2024 02:49:01 GMT
COPY dir:074f54b878561a19d242c8e2a7ebf93761c9ac51677c094a49834e516e5e10e3 in C:\openjdk-23 
# Sat, 09 Mar 2024 02:49:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 09 Mar 2024 02:49:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7da31fb9ae04d1a42010ec7341136b4fb44c7fdf5e26e5a3f9270b01ce5b48a`  
		Last Modified: Sat, 09 Mar 2024 02:49:22 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b91ede30f97de8a513b092cc373974a4c21a274f07294a70614d66aefb9614a`  
		Last Modified: Sat, 09 Mar 2024 02:49:22 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f87c324bd711b36fcb6d98aa9730475f2c9a787bf6e6fed7e3034768455a88b`  
		Last Modified: Sat, 09 Mar 2024 02:49:21 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630a40dd3153c9d415148a295817d82b6cfda76234420ec6c9fb41b17815613d`  
		Last Modified: Sat, 09 Mar 2024 02:49:21 GMT  
		Size: 70.9 KB (70894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084a25ee396bb087b4b8f850bd8036ec0d6bf2566dc3f0992a2e0a2e430e84b7`  
		Last Modified: Sat, 09 Mar 2024 02:49:18 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e31837c758d6c48a10dc8957a6e58f0b657ec469e11789fda07892a956a76d`  
		Last Modified: Sat, 09 Mar 2024 02:49:18 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480012675aa02dbfdea2f3c2da67500134d9ec927e1a1aeb2eaf0fdadf2d7e4c`  
		Last Modified: Sat, 09 Mar 2024 02:49:30 GMT  
		Size: 197.2 MB (197153249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e834ed00d490c1c3bdbf90c975ff8941f726682a13833f60b45cd0c973470b3`  
		Last Modified: Sat, 09 Mar 2024 02:49:20 GMT  
		Size: 5.5 MB (5488087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9636a0598bad3aa1c15f35f7040476eda48e8a7d873f6c06f846caca6e6665e`  
		Last Modified: Sat, 09 Mar 2024 02:49:19 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
