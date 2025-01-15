## `eclipse-temurin:21-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:9c4dc3069e99cea941a1eac5033caec1c4eff1aacd62bb7d3cacdbb61215bb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:21-jdk-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:9c66a90c94a7ec59d554473769addb0abe24707fe254a2ed5fa43e2b995e5d27
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.8 MB (361781032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0238ae5ebea413223b4f0d8a40e62649a5b9e4043b42f9fee6a17c0c6ea3f88b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:56:08 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 17:56:09 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 15 Jan 2025 17:56:09 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 Jan 2025 17:56:10 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 17:56:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 17:56:12 GMT
USER ContainerUser
# Wed, 15 Jan 2025 17:56:20 GMT
COPY dir:cc909cc6d9328a16dd1468618a073abc368d41e200a32534756819e3433a0b04 in C:\openjdk-21 
# Wed, 15 Jan 2025 17:56:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jan 2025 17:56:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472c054a782d18b0eec06a9d110587d787d33eb60621c48a7e6e1d44ac872bd3`  
		Last Modified: Wed, 15 Jan 2025 17:56:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9396536740a2810a03a2caf9ee4d18793bed2af5d9e0a6e02da098a6cbce88d`  
		Last Modified: Wed, 15 Jan 2025 17:56:33 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f3ab3a47ed855572c1915dc6c246aa48935e0c3e5a599a1358945862a9228`  
		Last Modified: Wed, 15 Jan 2025 17:56:33 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e99af066cdf4b79f973c81406abc2dcc2e2499c36a6e1d270ce24b07d758348`  
		Last Modified: Wed, 15 Jan 2025 17:56:33 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ff746f8819e4267c5b98d1506edee0ce1a9bd012ba40c174457da38d61dbb3`  
		Last Modified: Wed, 15 Jan 2025 17:56:31 GMT  
		Size: 74.4 KB (74364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460a636e73aba318be3a5592d72ff53d6abb485f55d0839a3bdc5097fe8c8ffe`  
		Last Modified: Wed, 15 Jan 2025 17:56:31 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8d7f84391f96070a5652e44f009362b8bf27f4351d83941d572ddcada0f27e`  
		Last Modified: Wed, 15 Jan 2025 17:56:42 GMT  
		Size: 202.6 MB (202575720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd1091734843efeb1e8728939e14bb8f0f944f68c1264d82a9b09055a9631b9`  
		Last Modified: Wed, 15 Jan 2025 17:56:32 GMT  
		Size: 3.9 MB (3857142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b66d7daba179f012291f7b3d6a40563bc53a20927e1e10fbb287070400fb8b6`  
		Last Modified: Wed, 15 Jan 2025 17:56:31 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
