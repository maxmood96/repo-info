## `eclipse-temurin:8u392-b08-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0ef850b52794d48bf382202d1fc7260577a515d8fe1ffe835d893f99faf0dd00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `eclipse-temurin:8u392-b08-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull eclipse-temurin@sha256:029a36d62621bf2dd416bbe7d3d483c29b1389ffae9da890399c2569ac1decc0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161019578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e40061de50ebf0c95d215db940636912f23dd4147a5c87a933a32aadba985ca`
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
# Thu, 16 Nov 2023 02:18:16 GMT
COPY dir:dbdf2dd9ed9894186d74b75beac1320724c73c6994b00118f04985f0ea2b3067 in C:\openjdk-8 
# Thu, 16 Nov 2023 02:18:30 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:2d323757cb3140bafadf6c3b4adbae81e732c6f80094a9bdf7bce1c79b825e44`  
		Last Modified: Thu, 16 Nov 2023 02:38:28 GMT  
		Size: 40.1 MB (40110948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a6f1b93dfa627fb1b5f26e06561c86a3d9bc1a8bd2ab81a43540fd55112e1b`  
		Last Modified: Thu, 16 Nov 2023 02:38:22 GMT  
		Size: 69.3 KB (69274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
