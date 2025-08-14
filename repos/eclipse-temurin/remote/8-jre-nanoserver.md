## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:3313b60fc9a97a584c75c1eebf18d6618595af4feae81996e227e74626094431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:50059989abead551f830f3dc8909cc6eda9236a8c60f6f6ce08a94aa68826092
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234194604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7720e4add91817ae1e0faf0134d6fb8db61c4e4f986c56a6396bc0f6ccd3a88`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:51:14 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:51:14 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 12 Aug 2025 20:51:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 12 Aug 2025 20:51:14 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:51:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:51:17 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:51:19 GMT
COPY dir:3a0e2241911cff37ef92eeb46012c4bf9f32f9301b3cfbba190d8fdd900a0568 in C:\openjdk-8 
# Tue, 12 Aug 2025 20:51:21 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63ecd9d2f1731edaf9a27e692969894f3290d48c87c2a70149c4083ddb58abc`  
		Last Modified: Tue, 12 Aug 2025 21:20:02 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd8883551d56ae0e276897e23003153ef708e4706de279a4564374f3211ab1a`  
		Last Modified: Tue, 12 Aug 2025 21:20:02 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5269b7ea2cb00045741c139838fb7cc1ca249354dd42f12f1b7f82451bf4ccc1`  
		Last Modified: Tue, 12 Aug 2025 21:20:02 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0223919863d4cb6c6ca94acdb0582d834795c7b456a9e5016700d9079804a2c9`  
		Last Modified: Tue, 12 Aug 2025 21:20:02 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7b3a746d4511324acd31d7ee23bc66136806a3b7dec38ae40e6439d95fbc66`  
		Last Modified: Tue, 12 Aug 2025 21:20:02 GMT  
		Size: 75.7 KB (75666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d97f726f18ba20f9b0135538f331d34bc14130e0968d95ce1799f49674766e`  
		Last Modified: Tue, 12 Aug 2025 21:20:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7b0349478962018c41a913e4f2a5eb0404a765e097768e3b3a996ed9bea783`  
		Last Modified: Tue, 12 Aug 2025 21:20:07 GMT  
		Size: 40.5 MB (40548198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22f3432f56086ebc5ea3c0c5603bb97a216dac1752b865889c0f1b4b795e308`  
		Last Modified: Tue, 12 Aug 2025 21:20:03 GMT  
		Size: 96.1 KB (96057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:617978d739498ed3120c2062476836dfe04147ed2a0f65e294353443a7a21eb1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163390763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fdf1c0f679cce45d74a57a2425a5b7752d374b533194f7f91c99bea147eba7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:49:55 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:49:56 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 12 Aug 2025 20:49:57 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 12 Aug 2025 20:49:58 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:50:02 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:05 GMT
COPY dir:3a0e2241911cff37ef92eeb46012c4bf9f32f9301b3cfbba190d8fdd900a0568 in C:\openjdk-8 
# Tue, 12 Aug 2025 20:50:10 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e520b634d8ee3eab66925c61f0e019e692e0fe212183172786a7eeb6b5c62ce5`  
		Last Modified: Tue, 12 Aug 2025 20:51:00 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7d5215baf4d8b057d49ba12fbaba74702a1881a1049fabcbd7f51d44262b77`  
		Last Modified: Tue, 12 Aug 2025 20:51:00 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e76d062bdf1ac2f015c11fe46438525e54921bb04a765ac802785d880a3be`  
		Last Modified: Tue, 12 Aug 2025 20:51:00 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25ac7afa6697848d6ffb94cfce7d1846cb5091cd37237cd724ceeec3b370621`  
		Last Modified: Tue, 12 Aug 2025 20:51:01 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2eb4ebc49738c03527748baca95a0cb52f8ab5946b2382bf1888a5f9727eca4`  
		Last Modified: Tue, 12 Aug 2025 20:51:01 GMT  
		Size: 76.5 KB (76452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb93f88c36b04951d32268e837e8d79fc3b2d44391342ff9a116548050f628e`  
		Last Modified: Tue, 12 Aug 2025 20:50:55 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94fc0edac43c2d4b4e992b82997ae78beb9bcb593a5d50b1f82307f1b9f73d1`  
		Last Modified: Tue, 12 Aug 2025 20:51:06 GMT  
		Size: 40.5 MB (40547823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc910a2e3136db383dfccc4e71cf73f780ebdd7012d5ada38fe115f83f86743`  
		Last Modified: Tue, 12 Aug 2025 20:50:58 GMT  
		Size: 101.0 KB (100970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
