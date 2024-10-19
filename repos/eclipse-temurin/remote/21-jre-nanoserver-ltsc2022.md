## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3962d8b0f3cebb78217be1ed1d60f63dd1a15aee41fd93feacc57a6b7a366f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:a983dfc580575dfa6161d9495675309742f7bb08d650334f98c5c284f0bdec55
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169338819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e03b79e265176c13613b180848bc6abf1d6b67364a027a687f74b8c54c6a87`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Sat, 19 Oct 2024 02:15:11 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:15:12 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Sat, 19 Oct 2024 02:15:12 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 19 Oct 2024 02:15:13 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:15:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:15:16 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:15:19 GMT
COPY dir:07997ead3a64c91435f0c829e99f4f88b0166c3faeab49d648d940e8c8333d36 in C:\openjdk-21 
# Sat, 19 Oct 2024 02:15:23 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bac693bae654936fe15dd687381d38f947fa8afb526204e11ea89f6c76038`  
		Last Modified: Sat, 19 Oct 2024 02:15:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27ecb367bbdc23f9b9a516d5316629d563bc99a8676efb17229e02f3d436635`  
		Last Modified: Sat, 19 Oct 2024 02:15:28 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee234e6abb87fd7f26c6dcf3f1b642035e6ad0e5cf1fd23aa58774ac28fa1029`  
		Last Modified: Sat, 19 Oct 2024 02:15:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d27ed986e040b8e085719fdc55f8472e596950c036b6b4771b39c7a3f4b43`  
		Last Modified: Sat, 19 Oct 2024 02:15:26 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8130dc99d9709eded97f7d96db20dc6ab20d7ee31853f0230d5c123827c3a26f`  
		Last Modified: Sat, 19 Oct 2024 02:15:27 GMT  
		Size: 76.1 KB (76055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d0b8d769c05878aa97fe0dcf4af57c7db83d1c32c813eaf03a3ad28e01f472`  
		Last Modified: Sat, 19 Oct 2024 02:15:26 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300d13611ed0518a9d60d84fadc177291754d529c419c5984be2d91a457ab993`  
		Last Modified: Sat, 19 Oct 2024 02:15:32 GMT  
		Size: 48.6 MB (48645782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87a2c0d1adff5ebc13f0d56fde39c69c8cc521310f19cc451a1746959908112`  
		Last Modified: Sat, 19 Oct 2024 02:15:27 GMT  
		Size: 100.8 KB (100833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
