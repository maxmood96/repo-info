## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:a4cf27010c6120aae3b25cf9efd5a83de6311aee8ebb6daff292c2f8360acd87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull eclipse-temurin@sha256:f596134901320d816c479aa8219cada376b1c4e60184d5c4d9d74c4f82f9abd9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 MB (201470262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb525106ed55bd0044e18dff1d6e8c275c8a52821c022cb2b4c631ab56c338c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 19:40:26 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 19:56:44 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 13 Aug 2024 19:56:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 13 Aug 2024 19:56:50 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 19:57:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Aug 2024 19:57:04 GMT
USER ContainerUser
# Tue, 13 Aug 2024 20:01:23 GMT
COPY dir:4243678b5415f703b690863e65df7851d84efb271bd792cb5cbd95ab7bb17263 in C:\openjdk-17 
# Tue, 13 Aug 2024 20:01:34 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee91db53edb9eaa638d7d926c33dc3d39a0bedf5ace2c9ff25f8c413bc3ea2c6`  
		Last Modified: Tue, 13 Aug 2024 20:30:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b70bfc9b4c4659e472565189e8686cc1358ab78d065c461cb01dd6cf481bdd`  
		Last Modified: Tue, 13 Aug 2024 20:34:29 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b1efbbf4248bf7b6aad5b53077d60c737ce55680e332e9a9ce4439cf27d86f`  
		Last Modified: Tue, 13 Aug 2024 20:34:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c52cae454d7cd1391842a420cdae62aa0b0dab7eab80bf93543cc06863a38b`  
		Last Modified: Tue, 13 Aug 2024 20:34:28 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf46376785ba215931564ba20d8c57e4aefe26493e0eec01066527d731c2348`  
		Last Modified: Tue, 13 Aug 2024 20:34:27 GMT  
		Size: 74.1 KB (74101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5a0819179419349ff009529d53fd977b8ce1de44e054e097aaf8feab6aeb74`  
		Last Modified: Tue, 13 Aug 2024 20:34:26 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39361ec639d8ceaf2e8a64673b4fa50337370998f9333e1fc46cc51cd73796f`  
		Last Modified: Tue, 13 Aug 2024 20:35:26 GMT  
		Size: 43.4 MB (43357674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91a51588effc89e8b11d1a93fb1ec572f43aed8421b145adb1651e82eba2889`  
		Last Modified: Tue, 13 Aug 2024 20:35:21 GMT  
		Size: 3.0 MB (2950059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
