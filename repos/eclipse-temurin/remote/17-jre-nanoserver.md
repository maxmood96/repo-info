## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ea0bef485000a7df8a4182f860606345f11337bbc88770f252e2d5bbdb2e9efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.2655; amd64

```console
$ docker pull eclipse-temurin@sha256:7614dd1a0aca1091cc0c0ac100412188d1500f26a3242d99f9df133789bdd110
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164061468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad93bde22e4c1acb3339844aea4b663cdc15fe9f7c54f5ad1fcd15812ac731db`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 Aug 2024 19:28:00 GMT
RUN Apply image 10.0.20348.2655
# Tue, 13 Aug 2024 20:19:48 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 20:21:51 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 13 Aug 2024 20:21:52 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 13 Aug 2024 20:21:53 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 20:22:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Aug 2024 20:22:00 GMT
USER ContainerUser
# Tue, 13 Aug 2024 20:22:41 GMT
COPY dir:4243678b5415f703b690863e65df7851d84efb271bd792cb5cbd95ab7bb17263 in C:\openjdk-17 
# Tue, 13 Aug 2024 20:22:51 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:695cae91f2de8dadf81c8b3a95f4942533ef064a72ad8fa7843cca84a839bfba`  
		Last Modified: Tue, 13 Aug 2024 20:02:51 GMT  
		Size: 120.6 MB (120554921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8146ec246b230c09f8b628d688c831ad1269b9cef24c5c95a8d1eb2f76b89bdc`  
		Last Modified: Tue, 13 Aug 2024 20:40:03 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20265a49d3dacdaaf58acb3e9f551f109c1019ea949cb7ffdffc7dec5409887a`  
		Last Modified: Tue, 13 Aug 2024 20:41:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78d85aed26ad3feee2724f6cc7a7e54ecfea6e0ca4e794cd7dcc1e0c7916676`  
		Last Modified: Tue, 13 Aug 2024 20:41:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac3d4120432f40bac72c7e3ed99c3a1cc93707517a3fafc4e6c133f7a74e5e7`  
		Last Modified: Tue, 13 Aug 2024 20:41:19 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a69350aef86f195e97a79fa5ccae1b19a1efcdfc900a0391207c1f6d6f8234`  
		Last Modified: Tue, 13 Aug 2024 20:41:18 GMT  
		Size: 74.5 KB (74536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576fcd1b5b1225af955db42b1899818f7ec96363fe5fdbdb94e8964b2d56a42d`  
		Last Modified: Tue, 13 Aug 2024 20:41:17 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b0303b5aff8b9d059d992641189a84d1f07d991a4d20e51a2ce757485df263`  
		Last Modified: Tue, 13 Aug 2024 20:41:47 GMT  
		Size: 43.4 MB (43364863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555d327c3a82303f8338ed132dfe34440bd1c1c7523a735e6deaeaf06a1eb7b6`  
		Last Modified: Tue, 13 Aug 2024 20:41:40 GMT  
		Size: 61.6 KB (61589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.6189; amd64

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
