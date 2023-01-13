## `openjdk:20-ea-31-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:391f7d2f525deaf2e8059cad02f75cd6372d9d91bb7c7b74f6612e29d96b1879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `openjdk:20-ea-31-jdk-nanoserver-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull openjdk@sha256:5e02717ab0b2c52d1d8bc960b0dc522f1ee4c80df114cfa875d7e44548efc2d0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303583008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37eeda627a010c03a22678e6e67ca5cf1fcca3294a997886278098731616482`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jan 2023 05:17:01 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:45:31 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 05:15:32 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 12 Jan 2023 05:15:33 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 05:15:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 12 Jan 2023 05:15:43 GMT
USER ContainerUser
# Fri, 13 Jan 2023 00:21:38 GMT
ENV JAVA_VERSION=20-ea+31
# Fri, 13 Jan 2023 00:21:54 GMT
COPY dir:02f69244990fbbbd49167a81f4d331e4df54083b76c45136446caabbdbbdc231 in C:\openjdk-20 
# Fri, 13 Jan 2023 00:22:14 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 13 Jan 2023 00:22:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e58f9ad3b15a2a4882ab0a845e8e619cc8c3c411ddbe8b50046c1618a95c1397`  
		Last Modified: Thu, 12 Jan 2023 02:40:44 GMT  
		Size: 106.7 MB (106666138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea67a6bd980bdee35399883e5abcc31c738b338ad384b2f92d91a15cf09d9df`  
		Last Modified: Thu, 12 Jan 2023 02:40:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96518e54215f38193b505640cdb2fef097c5741e65b4b97bba8f867e243d032`  
		Last Modified: Thu, 12 Jan 2023 05:25:44 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d63c92ba435f57ba529ea551f43866f6d4eba3a81d296b0fb044c740f2ee807`  
		Last Modified: Thu, 12 Jan 2023 05:25:44 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b356ba1f31bf25142c630cbcb07b081461c3f630e690d98dc24ae4786a9ef7a`  
		Last Modified: Thu, 12 Jan 2023 05:25:44 GMT  
		Size: 70.5 KB (70518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638383fe215678a48f17d26ca2a40f4c79f0e0929d53790d7d9d5d1d73cdb9cb`  
		Last Modified: Thu, 12 Jan 2023 05:25:42 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8aeff6d12dc1db0ba4832971a4c01d0cbd7deff5430daa181ba35282d08aa0`  
		Last Modified: Fri, 13 Jan 2023 03:22:17 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f0e88235c76e9f99f494f92ae4e964b6a02af2ea2d3c9ba785bb06a2bbb334`  
		Last Modified: Fri, 13 Jan 2023 03:22:39 GMT  
		Size: 193.1 MB (193062348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10d1fadfb99a4751dabcdb2f19ab4aa28b4d1aca4e77dfdc7421e13893e344b`  
		Last Modified: Fri, 13 Jan 2023 03:22:18 GMT  
		Size: 3.8 MB (3777530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc5c984116895d9495793f223863b26ba67ba312a7e3f7f3606da381ece3214`  
		Last Modified: Fri, 13 Jan 2023 03:22:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
