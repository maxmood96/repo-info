## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:44365e4a4652f03a164904ac4dd0fec71016bcabe9da905f7b3b15c2564b9f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull eclipse-temurin@sha256:0a65f5d53f858005c408598d4347401269b1537d4d1feb1c5aa3cf9d962ccb65
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146144556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea3f5b21be4f02ed0ab17cf396b8af3902b63770fda71c35eb65deedbfa50a0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Tue, 13 Dec 2022 22:53:34 GMT
SHELL [cmd /s /c]
# Tue, 13 Dec 2022 22:53:35 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 13 Dec 2022 22:53:36 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 13 Dec 2022 22:53:36 GMT
USER ContainerAdministrator
# Tue, 13 Dec 2022 22:54:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Dec 2022 22:54:18 GMT
USER ContainerUser
# Tue, 13 Dec 2022 23:00:09 GMT
COPY dir:4e862dd3e9e3173048336ba652726d009cc7bbbadd67bc711cdb421cf611c5ab in C:\openjdk-8 
# Tue, 13 Dec 2022 23:00:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:fd7c90f69f170db7a37913b13964bbbfb2834ee76b43ea9ca25fa1efb40b669c`  
		Last Modified: Tue, 13 Dec 2022 23:57:01 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7f3b3573c92322fe4ac1b6541ea5eb647dee960b120037d4b0e230a2f8cae2`  
		Last Modified: Tue, 13 Dec 2022 23:57:01 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c724f38c76f44159bbf01fc4bd23cfb20b7a39dea03a2f0ef59b42126231563`  
		Last Modified: Tue, 13 Dec 2022 23:56:59 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b57755d99e82b2b4bb1f95a6f7605e6dfc901e9678590246f818a39d4b35fd`  
		Last Modified: Tue, 13 Dec 2022 23:56:59 GMT  
		Size: 65.9 KB (65884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d2d761e2b4edce76f7b2324e5be67877fc6106bcb9c38982187f2836ebe0af`  
		Last Modified: Tue, 13 Dec 2022 23:56:59 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03682e5c3611bebdc916fe399051112977cbb80280074d6980f14b1f8329bbe1`  
		Last Modified: Tue, 13 Dec 2022 23:58:18 GMT  
		Size: 39.3 MB (39322732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8178107fa6bbe8c9b386d904d68d9481c9473626c746067279fd97e4d49ffee9`  
		Last Modified: Tue, 13 Dec 2022 23:58:12 GMT  
		Size: 79.1 KB (79139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
