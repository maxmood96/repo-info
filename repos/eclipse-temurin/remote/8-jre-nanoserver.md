## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4a8fdb2875814c02a3a497a564bc03209d6986f392a0cc81f68a727047fbe6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1366; amd64
	-	windows version 10.0.17763.3770; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.1366; amd64

```console
$ docker pull eclipse-temurin@sha256:b2b6097a4b75b4ed307a5a5dbe2073ff09d73a66f4d485180d5c0512d6f226c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161578743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17d5c4928947d4dfe369ba789a242c2a1232372ce1b4638eb4fa5c8183f5223`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Dec 2022 09:19:21 GMT
RUN Apply image 10.0.20348.1366
# Tue, 13 Dec 2022 23:42:18 GMT
SHELL [cmd /s /c]
# Tue, 13 Dec 2022 23:42:19 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 13 Dec 2022 23:42:20 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 13 Dec 2022 23:42:21 GMT
USER ContainerAdministrator
# Tue, 13 Dec 2022 23:42:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Dec 2022 23:42:41 GMT
USER ContainerUser
# Tue, 13 Dec 2022 23:43:28 GMT
COPY dir:4e862dd3e9e3173048336ba652726d009cc7bbbadd67bc711cdb421cf611c5ab in C:\openjdk-8 
# Tue, 13 Dec 2022 23:43:46 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:70d3e1cc3b0ea172dcc93064fe6fb9f1f2c8fec6962c90e39991fe89a3c1ca03`  
		Last Modified: Wed, 14 Dec 2022 00:08:13 GMT  
		Size: 122.1 MB (122108200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8147315b2e02d672b57634f58ed466ba0f8747ed03b8d3d40b71ddb17275cf`  
		Last Modified: Wed, 14 Dec 2022 00:07:43 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128acacdc09387e6d962a866eb39cba9f370a7b78476f914473b61887b1d89f4`  
		Last Modified: Wed, 14 Dec 2022 00:07:43 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb439320ce632121ee0f7a844774516fd648bdd0b2fd836a1cfdfc6005e25ab`  
		Last Modified: Wed, 14 Dec 2022 00:07:43 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3e95b11be8e1fe21a48fa16364d0ea798e51169c057d8e09dce1165481076f`  
		Last Modified: Wed, 14 Dec 2022 00:07:41 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787cb91bbed124848cabbf7aff1ceffd2f589690983d067f1b58e55704f45630`  
		Last Modified: Wed, 14 Dec 2022 00:07:41 GMT  
		Size: 85.7 KB (85685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd340f989f9d3800358445c493549519ae3fb410ab35b92c93fe00d61c66e06e`  
		Last Modified: Wed, 14 Dec 2022 00:07:41 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500e62c8245ed650a1c47d2e0777ef48d33088130bde5f6548c17f1ce0ed6c59`  
		Last Modified: Wed, 14 Dec 2022 00:08:31 GMT  
		Size: 39.3 MB (39322588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782a2a0f6ca9c97f90de8946b9c9a074592e491de8fd2a9c27595c9e331c0842`  
		Last Modified: Wed, 14 Dec 2022 00:08:24 GMT  
		Size: 57.0 KB (56996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.3770; amd64

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
