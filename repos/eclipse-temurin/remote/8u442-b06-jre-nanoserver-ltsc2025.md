## `eclipse-temurin:8u442-b06-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1a3767ac4db7b470dc1d216bb5302c6a0510b83749f5689bbbb06c4050e87d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:8u442-b06-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:b8b955c93ddccaa17bf55a2570b6ca502a5f9e45c04aa9faca5b9e2200e5f1b8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230839639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ba40aff19fa6452b5e8fe13016c290d4bf309495f9555e5065cfecefeb5b62`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:17:36 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:17:37 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 09 Apr 2025 01:17:38 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Apr 2025 01:17:39 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:17:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:17:42 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:17:45 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Wed, 09 Apr 2025 01:17:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d359084aa46c27da8504967579b6c10642ef236971754e03da5fb98f14265d`  
		Last Modified: Wed, 09 Apr 2025 01:17:55 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e9bb659181740fce4f82e4bc60cd345de47de8967bd7204ee1719a6627565a`  
		Last Modified: Wed, 09 Apr 2025 01:17:55 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac118af9931455b122b05c02e048e17c5f4fee342c9735d172e21c971cef1abe`  
		Last Modified: Wed, 09 Apr 2025 01:17:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0787a7b73ed50be70ec8e8d3d0f387b11ce693f20a573689aa7cd062b4c9cb98`  
		Last Modified: Wed, 09 Apr 2025 01:17:53 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8872db4b3fb1b456db3f5d9401f41b189aae998c43c6f7c4bb222278e2fe87a`  
		Last Modified: Wed, 09 Apr 2025 01:17:53 GMT  
		Size: 76.1 KB (76092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c02796add8739739d9900f160ff233d3c8136f181d310e3b435a3b47318516`  
		Last Modified: Wed, 09 Apr 2025 01:17:52 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ac9154a569806eb7563faf95f76008dd6b5127ec9ad5f7c7a28a9afb618b26`  
		Last Modified: Wed, 09 Apr 2025 01:17:56 GMT  
		Size: 40.6 MB (40552519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47924eca07819d04efa9450504795e68b49324d416546b05dd3011c706296080`  
		Last Modified: Wed, 09 Apr 2025 01:17:53 GMT  
		Size: 92.6 KB (92612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
