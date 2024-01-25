## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:db5363f8610c91f083bc5014586374c2a585cfe0551c34f85e28ae7545ce2374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:9a8177c235c0e9333b80a89e2c567b7ea1e858f89d7525241472028d9de7e386
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222613027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e01e31d2bd9331f2b83fd9ee205e381239b4fa2969e88443688609d88eafc16`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:53:23 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 21:53:24 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 24 Jan 2024 21:53:24 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:53:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jan 2024 21:53:47 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:53:59 GMT
COPY dir:9ab35a15e19e8247451d444f7de2a75fe407ec1749c1b49082dcaaef6c80dafd in C:\openjdk-8 
# Wed, 24 Jan 2024 21:54:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5f2601f3a3b05b34c1f8683e3c9ea81ea63dbe1b04c37b85d09170f020fc0`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bc6f55d94ad6babb64b648ddd4e3d6d8072a6266be4c48a8381f0c374a7724`  
		Last Modified: Wed, 24 Jan 2024 22:11:23 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8550800dcda4ebc8d1cc88204963b26f3442312b25f671aac3d9560aa39b4df2`  
		Last Modified: Wed, 24 Jan 2024 22:11:23 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520937eeb616efcc621cdf2db195eef5183f5b7517ef9ccf1a110e4eb1c01c39`  
		Last Modified: Wed, 24 Jan 2024 22:11:21 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c41f39f8cd5ecc958ed1cad2cb8d774b184e8e399d3ad9b793e5a98904d4a6`  
		Last Modified: Wed, 24 Jan 2024 22:11:22 GMT  
		Size: 85.9 KB (85881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605c359866d83e1868c6b725a8294b3ff8f2e73ae0272190ab7c80a25ceb1d9b`  
		Last Modified: Wed, 24 Jan 2024 22:11:21 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22219c15359581eb8e900bafe1c1759cfe3f0b92b19c0500c6a200848ed3acf5`  
		Last Modified: Wed, 24 Jan 2024 22:11:33 GMT  
		Size: 101.7 MB (101693459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fca4d37651ccb6fdbe55d1278fe9d63a9d1149ce1f98370e57e80b1a6e9642d`  
		Last Modified: Wed, 24 Jan 2024 22:11:22 GMT  
		Size: 58.7 KB (58675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
