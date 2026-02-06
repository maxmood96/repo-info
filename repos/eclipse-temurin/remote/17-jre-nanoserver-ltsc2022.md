## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1ef1101bae04224aeb9f12ca53489af524e4c91c84bc809d4f30c704b32690a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:cb198e216cc36047698aa7fb48a5658ab51002d26b282a6237e3fa4f95aa1c7b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.7 MB (170676223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9079b194927921282b10b585baf1cd7bcaae7a532201d3dc82328ae9e39d4b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Thu, 05 Feb 2026 22:39:20 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:20 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:39:21 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 05 Feb 2026 22:39:22 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:39:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:39:30 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:39:45 GMT
COPY dir:064fca0b30194d02fe341355ba6a62fc1748c82418561395eb5bec357779f4c8 in C:\openjdk-17 
# Thu, 05 Feb 2026 22:39:50 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cd40533ff3016f01489a6939469bddb4641fc5207f54c664a403d02ebbf2cc`  
		Last Modified: Thu, 05 Feb 2026 22:39:55 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203ae6b7dfeb900605a0b42a0ffc860ef18a1efb243d4435fd4e065ac7e0d940`  
		Last Modified: Thu, 05 Feb 2026 22:39:55 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91b7b2c95e85d1fa336ca2acba4d99fc2b0965dddf2864a75edcc33ca951f1e`  
		Last Modified: Thu, 05 Feb 2026 22:39:55 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf88023f00c16c1c68d23aa768b63b4be7fb300cfbeed5c1daf3e018f805ec8`  
		Last Modified: Thu, 05 Feb 2026 22:39:54 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296517e9e6b4ca2fbe8d864a998d2fb6ad158944dc8dc888f4dc56be39d69ee7`  
		Last Modified: Thu, 05 Feb 2026 22:39:54 GMT  
		Size: 71.8 KB (71802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d016f0d67e51b4e47eaf0c60970cc18a4fb69615e2e34b1785b288ff70eccd6c`  
		Last Modified: Thu, 05 Feb 2026 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7678327354b147518a4ff7454e843860b19697716cc3524400f77ebcc48f0226`  
		Last Modified: Thu, 05 Feb 2026 22:40:00 GMT  
		Size: 43.8 MB (43794747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f5b04ec5508c0faac599566d3182b430debeb6b1b0d96959babece00ef6a00`  
		Last Modified: Thu, 05 Feb 2026 22:39:54 GMT  
		Size: 107.5 KB (107500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
