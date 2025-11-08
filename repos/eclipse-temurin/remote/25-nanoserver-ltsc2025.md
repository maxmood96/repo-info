## `eclipse-temurin:25-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1108d7027d2d2f6e9c07ab026567bec1dc80817bf38709cf0776debfc450c83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:25-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:ddc90e742829f6a09a27b7b3cbccda8f6264df95f477648759b451e92bc55240
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.2 MB (332183481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0defa6f3b069c9746efe29e5e0cc23355e4f2c04493e8278e8af36b3a63a05`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Sat, 08 Nov 2025 19:19:14 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:19:14 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 19:19:15 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 08 Nov 2025 19:19:16 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:19:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:19:21 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:19:32 GMT
COPY dir:889642903e29f32ff0f0b6da5f64cf6a40ecfa6d85d0926e4981ccbc885ac0c0 in C:\openjdk-25 
# Sat, 08 Nov 2025 19:19:37 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 08 Nov 2025 19:19:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3951beddd0c036c165f339869dab951299b53cf4f438eddd55b5e2b052fdbde4`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b5d7f9a8b981ff980132e2156290054354c4d2a91a7d88c17e1592c4c4aa95`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4047690f7787dd3fc91c1981bc70dc2bb9c487ced3247436c157e9107353083a`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890835a7dccc965ed75636c925c94e7745ef856656e35f89e85fbf134f7a3560`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4f187879fa93e43326132627e37a7d95190d96ea74ad0461325e0c39e63956`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 69.3 KB (69319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fb06392818817993f818c9b988827d54081c9a15efb5c0d56d39683d4ae37c`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002006204fc4d4e28a75cc4b95e2486e57f3762739f55bc4f04ac0aa39832d51`  
		Last Modified: Sat, 08 Nov 2025 22:21:15 GMT  
		Size: 138.0 MB (137952154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe5d2f7a5dbfb35d47595d1cd2c7c9b0657e635308b39d5ea22bcf73684cdc6`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 126.1 KB (126123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8433ef188efc6f2c42d7ab1e6fee64d21bf2b3b21c462ee77725ff648861c1ae`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
