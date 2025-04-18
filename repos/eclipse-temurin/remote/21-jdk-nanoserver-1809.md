## `eclipse-temurin:21-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:5b1e0a387090daa18788132de5b88cdf0f93ce8c678fd445c7f30b45d8d54b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:21-jdk-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:e7fb8b7d59b195a464d2f7fe1342dcba855e52c61e114a462a53fc0183ca2f89
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314120051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d23f7d0b0413ac2faf833bf50d70da5d74c5a58bc03a8a5c9220698d03f1dd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:17:07 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:17:09 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 18 Apr 2025 04:17:09 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 18 Apr 2025 04:17:10 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:17:13 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:20 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Fri, 18 Apr 2025 04:17:25 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:17:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c13df5f4348ca3a97f85905cce89c2cc01f8e249e683767f0a95feb84fef947`  
		Last Modified: Fri, 18 Apr 2025 04:17:30 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f67bcc6dc549dc30112f5c61ffc01e3283d66bffcec4d5ba19c9b44d959c`  
		Last Modified: Fri, 18 Apr 2025 04:17:30 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af7ec33d1da800f1d643723547078f8d74a3fcbec8278764eb61c64aeb18e9c`  
		Last Modified: Fri, 18 Apr 2025 04:17:30 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0552b2903fcb5a73827248e9877e24d6be6a675bdd775938df044996ddfc8fe6`  
		Last Modified: Fri, 18 Apr 2025 04:17:29 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22caa57540576dcae253ea93595719606ec13953d79f6a79885ac0578fbe6e13`  
		Last Modified: Fri, 18 Apr 2025 04:17:29 GMT  
		Size: 69.3 KB (69306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478586a536f00e11f3c2aba47eab51a3db812108679fd6d9ecc30198483cbaae`  
		Last Modified: Fri, 18 Apr 2025 04:17:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ced69b6f125cc577e28b96f88b566da184e405e208458901cf179c7a0d9ad1`  
		Last Modified: Fri, 18 Apr 2025 04:17:40 GMT  
		Size: 201.5 MB (201475954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d52126d2b0f7ab2ebff4e192ccfb641d60e1e26030a2dc07c653ba00093bc9d`  
		Last Modified: Fri, 18 Apr 2025 04:17:29 GMT  
		Size: 3.8 MB (3816323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0716ef4505b43a8bc5c4f79ce4a179e9e159f0a98b09ca8f56fad87efdebd900`  
		Last Modified: Fri, 18 Apr 2025 04:17:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
