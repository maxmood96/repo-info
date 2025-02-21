## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:05f7300764550a55b5d1cde26d285309bf8143d03df7eab89469675bcada62e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:b975fae58d69b9d73ba37be1135b7242912cce2dd2ea40ddabdd66c9feb9e3dd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393801078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45667f9b181f584bee0a2ab032df61344b5374ee68bdb942d53550ebe0adfe5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 02:16:40 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:16:41 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 02:16:42 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 31 Jan 2025 02:16:43 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:16:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:16:49 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:16:56 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Fri, 31 Jan 2025 02:17:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 31 Jan 2025 02:17:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf4cac08657e35f531d4d122b5dea475e3fcb8473a30c2d0b98694e65011bf8`  
		Last Modified: Fri, 31 Jan 2025 02:17:10 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ec2b9e65e8712b8f0e30b631f7614cba427aa7084a52ef53924d801a7b5f71`  
		Last Modified: Fri, 31 Jan 2025 02:17:10 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdce1f6ae7973a405d5172cd6a657ad2161ce15105a2204e99c2c1d6b7ee8ec`  
		Last Modified: Fri, 31 Jan 2025 02:17:10 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c24debb0cfbf08a5908319a43f11dfc9e4e3cf25df28ae2d717af653bd137d`  
		Last Modified: Fri, 31 Jan 2025 02:17:09 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b75727cac3d511d96c604cb484f14adfe06edc58bed0c0533b4d361da21781`  
		Last Modified: Fri, 31 Jan 2025 02:17:09 GMT  
		Size: 76.2 KB (76241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38e63857b81a33b940431536733517488c6157adb542b1c6fa1cb654b0364e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:09 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04163d4be6ee7ca67ed67e04b3170f729e0394b4e2935844e9f65b3f6963da57`  
		Last Modified: Fri, 31 Jan 2025 02:17:19 GMT  
		Size: 194.6 MB (194557242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227318206d3b582ef3d70a6a1f7be95cd3867a2a3b383ae9f7232302b6341f67`  
		Last Modified: Fri, 31 Jan 2025 02:17:09 GMT  
		Size: 107.0 KB (107019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6bcd98ceef5031a4346422c80ef0791241d37aad2b53fc8a2b68ebb27906a`  
		Last Modified: Fri, 31 Jan 2025 02:17:09 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
