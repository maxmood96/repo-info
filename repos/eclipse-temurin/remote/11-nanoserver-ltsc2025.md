## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:36a5f10fd9b4769685ed21753986ff4389e1274bd79fe1ac27763a7b06d0937f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:d3bfd8458d54e8dcf1849e5724455f55c8e0d0772482963f6a41ea2010c2eda4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.2 MB (386187220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ef48f0d8998a74c62d7aa4745285f694b1e8f561d3e51723c62543474142b5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:14:36 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:14:38 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 14 May 2025 21:14:41 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 May 2025 21:14:44 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:14:54 GMT
USER ContainerUser
# Wed, 14 May 2025 21:15:04 GMT
COPY dir:c61af6ceef573b3d63f31a61f55e07ef4d3bfab78d8c06e63a667655942ae5e8 in C:\openjdk-11 
# Wed, 14 May 2025 21:15:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 May 2025 21:15:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6ca752ec3a3f8179cd29c04db4ca122a2189bf821eaa9fa16f497ef96d3c41`  
		Last Modified: Wed, 14 May 2025 21:15:26 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5640c811c6efbe2fa37557c6621895bf8e3b1b625f964c89179bb096c9e49b5`  
		Last Modified: Wed, 14 May 2025 21:15:26 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6e0d63fdfa4f5187fbda6a606f652947c9b4c6122f0b01b4b8c28632fb6d3e`  
		Last Modified: Wed, 14 May 2025 21:15:26 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3745283007aaae1efcdcbec55d2ed032c8a33a3cba50e09c8806a892bcea40a`  
		Last Modified: Wed, 14 May 2025 21:15:26 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5dfb53305df1e12174e5f0dc32a2e4110a66a2657018cfc0d97671e96ef1a7`  
		Last Modified: Wed, 14 May 2025 21:15:24 GMT  
		Size: 76.3 KB (76292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc9e7592d190694752126b2c8a8c01e110f7a6b91204cbc4cd3acae24023c3d`  
		Last Modified: Wed, 14 May 2025 21:15:24 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851f8fca13bcfd447e4778930dd024e64ea0ce196daf4d60d734473b8b963439`  
		Last Modified: Wed, 14 May 2025 21:15:34 GMT  
		Size: 194.6 MB (194577637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3628c51c5d499670902f350405f8c57140ff8c320e73c8cfe62f4ec5efaa88e`  
		Last Modified: Wed, 14 May 2025 21:15:24 GMT  
		Size: 115.0 KB (114981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e9cbe4765f98f4f6c809a513afd16d106da0de5b27fdbfd0c0984e24fcde78`  
		Last Modified: Wed, 14 May 2025 21:15:24 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
