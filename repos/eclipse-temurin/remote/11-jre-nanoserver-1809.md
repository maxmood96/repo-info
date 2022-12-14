## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f43997c5929df38eb5a075404468be0ab8a88c75e42d0a8d79323c92a94fdeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull eclipse-temurin@sha256:409c2843cb5085c40a973fd3e7c3601ea9f1bf47fed3c6c1e18e85207b14fa69
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149777311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856c42d0e7a8df5aaea9ae5c33fb5209a050540af4d58a0e77b5d2bdb0afe22`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Tue, 13 Dec 2022 22:53:34 GMT
SHELL [cmd /s /c]
# Tue, 13 Dec 2022 23:06:46 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 13 Dec 2022 23:06:47 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 13 Dec 2022 23:06:48 GMT
USER ContainerAdministrator
# Tue, 13 Dec 2022 23:07:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Dec 2022 23:07:11 GMT
USER ContainerUser
# Tue, 13 Dec 2022 23:13:28 GMT
COPY dir:f12bd30467bc1b7f61ca05a6124e6eb838888f3685c56f372d6fed2165b193b1 in C:\openjdk-11 
# Tue, 13 Dec 2022 23:13:49 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fe06cbef5ac46e54edd743daf1bc2bfa36b294c7ce9104837061c41a4bde7b`  
		Last Modified: Tue, 13 Dec 2022 23:57:01 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb8524c91bdbf6a7a33e8c0ad6dad828d186e06a513c2edc0678733ecb0f99`  
		Last Modified: Tue, 13 Dec 2022 23:59:52 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f983c21c22b46f2e7d5dffede9b9dfbd2cecbcb93b6f9c23bf737df01f17c8aa`  
		Last Modified: Tue, 13 Dec 2022 23:59:52 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5445aa3c23341b2d8090d1feb4c090e6cd90823d351d51e4ba41cb0e54b6f771`  
		Last Modified: Tue, 13 Dec 2022 23:59:52 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea8c2e4adcdc5be061df670c2a0ef13fa38bcf5974b92a3e082a835cdc352cb`  
		Last Modified: Tue, 13 Dec 2022 23:59:50 GMT  
		Size: 66.3 KB (66268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62b804a7a14a42abc99335def4bac7efc35e7ccfa62f76bdfa64c00727ecc1b`  
		Last Modified: Tue, 13 Dec 2022 23:59:50 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c8584b1f17c29e58e0a183e4604924252ac0fe6b8100c8aa1ae656135cda90`  
		Last Modified: Wed, 14 Dec 2022 00:01:20 GMT  
		Size: 43.0 MB (42954833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c742f778faae668e0e9600cdc804367062e20bfe8d89c5e18859aec1b2d674e8`  
		Last Modified: Wed, 14 Dec 2022 00:01:11 GMT  
		Size: 79.4 KB (79362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
