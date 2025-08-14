## `eclipse-temurin:8u462-b08-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0c23c1253928e7f2520ef241df0f50f8f58925f170779e68256381be96fde24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `eclipse-temurin:8u462-b08-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

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
