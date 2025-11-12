## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a087e43cd49f164fde465754740fb13d952d921561502e6a3d1ae479066086fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:f7610939121255d7751b94b5ae4cfd106e240085cb679110614b75eea5ff6650
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238687014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32132a862605da90d120fc0c221c632fe1235835d5a6b6884ade781b0adc240`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 11 Nov 2025 20:10:42 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:10:43 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 11 Nov 2025 20:10:43 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 11 Nov 2025 20:10:44 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:10:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:10:49 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:10:55 GMT
COPY dir:d46ae848a780de83988aca6679aeefb6cb592f306ae2eca344ddb66bc6559a89 in C:\openjdk-8 
# Tue, 11 Nov 2025 20:10:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82420529eec49d9844e6bcea0ba1c55c2202b9d70f948ba02c97b7dbbec9579`  
		Last Modified: Tue, 11 Nov 2025 20:11:47 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ede63081d279a805c1ab5ce2d3c57bdf4b81d4b483583b262cfea3ede65949`  
		Last Modified: Tue, 11 Nov 2025 20:11:47 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ae6f011fb0d8525b8ed0c08611d382285405537d6447d1918f062e4afa5895`  
		Last Modified: Tue, 11 Nov 2025 20:11:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2502e93451cafe198ecab0ccf13e26cd764d812c32ed386448f2cc4c280839`  
		Last Modified: Tue, 11 Nov 2025 20:11:47 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4995c6a65df78d1c7bf6e05a55ccac285308dd1bf870f5cb8a556b5c0d6b94`  
		Last Modified: Tue, 11 Nov 2025 20:11:47 GMT  
		Size: 76.6 KB (76635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ca261f2020f9dab8330fb0a10d266da13822f604bf20408cbf14eb20d48252`  
		Last Modified: Tue, 11 Nov 2025 20:11:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4214a8b78c7d4fbeee15124dfe0c7db78392e6147017c0ceb483b59ee90d330`  
		Last Modified: Tue, 11 Nov 2025 20:11:50 GMT  
		Size: 40.6 MB (40555284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29ee9db8161bd274a306dd41dd4bac76078eca3fb32705bcfdaa305dfeafe2d`  
		Last Modified: Tue, 11 Nov 2025 20:11:49 GMT  
		Size: 113.3 KB (113302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.4405; amd64

```console
$ docker pull eclipse-temurin@sha256:980798d22f512b0ee72cdc8f76670a39d2b94176f9525f9f96841ee43bcef028
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167086002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e74af986c75c5765e6600623667eac1eea848ff205a928bd79aea5dbdeed18e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:50 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:10:50 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 11 Nov 2025 20:10:51 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 11 Nov 2025 20:10:51 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:10:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:10:53 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:10:56 GMT
COPY dir:d46ae848a780de83988aca6679aeefb6cb592f306ae2eca344ddb66bc6559a89 in C:\openjdk-8 
# Tue, 11 Nov 2025 20:10:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d16ceaa756e1355602fb04abbf1e5a5b08eb674963f112eadbd9c9aaece04d`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44d9201be9abf76e4f3c486903dbd92a4bc2b4d06f166f91d00dc5b524f8926`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23311eb63ab365c9418f09b30c90e51540a5c6cf37b0bd4781bb33a59cd042e5`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17110e60d0f456958dd2a836c0e3b133f3eeb602f39b16c6673cc66bcd46ac43`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871b56a8d2c3f19ec44c3c1146604e735ede56d29783558652e67865a584e5f7`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 76.3 KB (76307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6ada554f82d23a80cc392e482cd47a02c3f4cbd8bbcd7e4ff766e39bdc3444`  
		Last Modified: Tue, 11 Nov 2025 20:11:33 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4bd7330fea3cea6e4fd8b028855ce52ea3d86adeb5cac88e72b88503df96b6`  
		Last Modified: Tue, 11 Nov 2025 20:11:38 GMT  
		Size: 40.6 MB (40555105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41156719b400605d88d6baaa76c97a79452845b22516f2d25a9e1b5065f5b1`  
		Last Modified: Tue, 11 Nov 2025 20:11:39 GMT  
		Size: 100.2 KB (100238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
