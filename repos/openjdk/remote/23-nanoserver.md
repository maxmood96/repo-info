## `openjdk:23-nanoserver`

```console
$ docker pull openjdk@sha256:4f38c1b683d58675d012777c3476d8494a672c5d05cc5424c1eb2f8c1ff5cd59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:23-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:f068e41d3969c6785d1ea5d7e74031b6bc4f227568ad58317b2c7c537318b6b8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306081131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55ff400a658c72f2af1f8cdc2bc6fd5180b96e64f6956ead4802c163ea76df3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Fri, 23 Feb 2024 19:51:35 GMT
SHELL [cmd /s /c]
# Fri, 23 Feb 2024 19:51:36 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 23 Feb 2024 19:51:37 GMT
USER ContainerAdministrator
# Fri, 23 Feb 2024 19:51:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 23 Feb 2024 19:51:50 GMT
USER ContainerUser
# Fri, 23 Feb 2024 19:51:50 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 19:51:58 GMT
COPY dir:0cd4a796a25a81bdedee53a41d48d913c0c3a34d3e4cc0e3f3914308953946b6 in C:\openjdk-23 
# Fri, 23 Feb 2024 19:52:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 23 Feb 2024 19:52:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2478835b6318cf72b1a30c62abff5e59fb5548d28143501cb6085f7665a48d`  
		Last Modified: Fri, 23 Feb 2024 19:52:12 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ecf8bfdaedf55d98dc84dd7e5c23167dda39b724efe6453436ca4f9a4d2ce0`  
		Last Modified: Fri, 23 Feb 2024 19:52:12 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75cc8adbafe62da19c0c595140349faabcd1a2f4b812dcb0ebccc55220c50db`  
		Last Modified: Fri, 23 Feb 2024 19:52:12 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2725ae20b003b9502deba776d2663f9e6556454eb0a80ae3e0016e8cd7963e2`  
		Last Modified: Fri, 23 Feb 2024 19:52:11 GMT  
		Size: 68.1 KB (68061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67c12fc083e257a7159055d4ac94af9461a45ae5234d0dd80cab9f483c42cd1`  
		Last Modified: Fri, 23 Feb 2024 19:52:09 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebad45a157937fd600404b1d08050ea1e66094bbb98dd4e884d8ce9a63eb40d5`  
		Last Modified: Fri, 23 Feb 2024 19:52:09 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b717c2484b15753f15ac03dec1564b9190956cdda8853661d91ce4d16a2a389`  
		Last Modified: Fri, 23 Feb 2024 19:52:20 GMT  
		Size: 197.5 MB (197537795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6b1e54ade64d2385d3f666afdc15d23df535812c655e3f09aed79dd6e69d76`  
		Last Modified: Fri, 23 Feb 2024 19:52:10 GMT  
		Size: 3.8 MB (3847434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61842e135e70bf0c5f3364f5b6135ec5a177c40c43ed6321c10a86ba5f96495e`  
		Last Modified: Fri, 23 Feb 2024 19:52:09 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
