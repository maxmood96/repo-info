## `eclipse-temurin:24-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:890f3b65f7059483f89156da6a8f8992ee5c7bbcb4a3a74ae9eaabc9ca2cfa5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:24-jre-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:a5e7154c2d9bf90be50d707d60b976e634f5811cb88bddc608d00255a5beceec
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168603554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30cd24cfbfec888640e6152106ca42953b29498a6b4c77cf9292d92b67dc350`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:20:41 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:20:44 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 01:20:45 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Apr 2025 01:20:45 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:20:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:20:49 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:20:55 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Wed, 09 Apr 2025 01:21:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcc6759b25e1ff0cb6cb4f455e94ecd27b2c8777349a97d384ceef85d3362cf`  
		Last Modified: Wed, 09 Apr 2025 01:21:06 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9b6e6f038ad2b7ee9870fda7633c9268a6022e6108093e8b7e6a5aa9946014`  
		Last Modified: Wed, 09 Apr 2025 01:21:06 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8a71b21b417161467f59de1278a51e6fb01e9cd2aa44b09fadcd2e130f441a`  
		Last Modified: Wed, 09 Apr 2025 01:21:06 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd80c339caa441f724ad6fc0408fa3275abb5cff18a6f765a08ab3f02642876`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf7324b467845202a6772835ad25f62a7c29932561abdb49fde4211d08c7e90`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 69.4 KB (69412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167003c646c376dd536f1a0210b6c431a6dd765e7ae3a21569ca1174e868ef8e`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e52164e67e137d88a1d63df22df6b0dc47f0fc5f33c252aa64443afa366b1b`  
		Last Modified: Wed, 09 Apr 2025 01:21:12 GMT  
		Size: 57.7 MB (57701210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d207b5570d306038823001e29275ec993d4f9efa056cd57411513539b6f43270`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 3.9 MB (3905050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
