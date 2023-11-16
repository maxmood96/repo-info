## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:393cb60d33d83df1488c40fd66cc80eaf574997ffd90567616ecdf2a466491d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull eclipse-temurin@sha256:c7703807fa0893861f2c922fcaeb0f11cc590c97774882be9b87ec980a77e99e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222605211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6db69b3f30ba16db9d417eba746baf7147e0b8889c91d840c603f5b1e21f23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 06:09:19 GMT
RUN Apply image 10.0.20348.2113
# Thu, 16 Nov 2023 02:17:18 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 02:17:18 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Thu, 16 Nov 2023 02:17:19 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 16 Nov 2023 02:17:20 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:17:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 02:17:35 GMT
USER ContainerUser
# Thu, 16 Nov 2023 02:17:46 GMT
COPY dir:d9c44d909d2b41aad5bf6fa4f7c7d36e81063822ae5e7ef30e4851bbe7809503 in C:\openjdk-8 
# Thu, 16 Nov 2023 02:18:01 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:1ca4fbe907f22e883670decfa8d7f4490a79a995bb83a6c286248c21d61a62f5`  
		Last Modified: Tue, 14 Nov 2023 21:13:36 GMT  
		Size: 120.8 MB (120753560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2f0edb58e1876347bbad88c907697db94e172aa6ff4a38560ccfb68d72aa86`  
		Last Modified: Thu, 16 Nov 2023 02:37:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b06c7fcd4b77678504c4ca400ce6d60d1dcd4b0bc189082188b0a9b175a1f8`  
		Last Modified: Thu, 16 Nov 2023 02:37:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f20a83e1a7a05ad64e315e8e7b5aedc11ab7e9bacaf3858ccba18cb2b73c21`  
		Last Modified: Thu, 16 Nov 2023 02:37:47 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149342164a2c9d519e19b8a43c2de06a781fb62c876ec017c217a30331c0849c`  
		Last Modified: Thu, 16 Nov 2023 02:37:45 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba6e798dde055059267cfbed9297c0341c464b2ee831d656b18fbbfd095f30d`  
		Last Modified: Thu, 16 Nov 2023 02:37:45 GMT  
		Size: 80.0 KB (80005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bed9fcf2ed9ba56fe06aa5ba78f80582a9a64ea14044cb1d89f00f596748e8`  
		Last Modified: Thu, 16 Nov 2023 02:37:45 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a88c3121f7954bfad950bfaf66b09a0f00099ab055f13e6c0eb52e97bde82e`  
		Last Modified: Thu, 16 Nov 2023 02:37:58 GMT  
		Size: 101.7 MB (101696658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27772829380cdd0daa9f25c553a880d6cde1c38b073feac6c964520eb4ec5223`  
		Last Modified: Thu, 16 Nov 2023 02:37:45 GMT  
		Size: 69.2 KB (69197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
