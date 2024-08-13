## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:95fe0c901de7e01d9a1337a3b130606e930f325a7b0e07f8b8725f21cd404270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull eclipse-temurin@sha256:f6602478993cd515ed5e644dd1639aa26bdaaed4320bbc9c23a50d43c3972b08
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345205930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532e0a048f8b895d61d0f39da0612b8be0d00f4def10b63e41e3866b4b9f7ddb`
-	Default Command: `["jshell"]`
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
# Tue, 13 Aug 2024 19:57:22 GMT
COPY dir:11f935f87b5561ba9de5a02e585d9b073f4114e9ab1765209f28e6005e01c91d in C:\openjdk-17 
# Tue, 13 Aug 2024 19:57:32 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Aug 2024 19:57:33 GMT
CMD ["jshell"]
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
	-	`sha256:3a742c8de2a64e8119b92fb8f425cc79b161034f8a3887b729bbc20bb9578f6c`  
		Last Modified: Tue, 13 Aug 2024 20:34:40 GMT  
		Size: 186.5 MB (186456025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72cab196782565d4ffb9eceda14796f550ec82d234c6a4add1a2e0d57dbe960`  
		Last Modified: Tue, 13 Aug 2024 20:34:27 GMT  
		Size: 3.6 MB (3586341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b6ab79fa05428bec7689638da90660834f99df15a456c4d4dcc851baa6ac8f`  
		Last Modified: Tue, 13 Aug 2024 20:34:26 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
