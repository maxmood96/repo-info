## `openjdk:23-ea-8-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:7c71372197194e1195e94a523398f7970238c8f70c3aca2ee84b12a4b9501982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:23-ea-8-jdk-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:2a000098c47a91125cf04e98c94db67f8b9e91d24726d05db12a8718a06396eb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (306013485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37df408d752424cc08728dfa2632437f7ccfe278454c1faf01de2165fedb0193`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Fri, 02 Feb 2024 23:53:42 GMT
SHELL [cmd /s /c]
# Fri, 02 Feb 2024 23:53:44 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 02 Feb 2024 23:53:45 GMT
USER ContainerAdministrator
# Fri, 02 Feb 2024 23:54:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 02 Feb 2024 23:54:03 GMT
USER ContainerUser
# Fri, 02 Feb 2024 23:54:04 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 23:54:13 GMT
COPY dir:6a84c5cee471a7abf9cef5fcb4872f5f6ecc20119671264fac429d350b8b4ca7 in C:\openjdk-23 
# Fri, 02 Feb 2024 23:54:19 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 02 Feb 2024 23:54:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb25363684c40bc2d1539ee270401cda56fa2210c5f9146f5dc783b2d19a750d`  
		Last Modified: Fri, 02 Feb 2024 23:54:24 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05d98f30d9e93456c938cbeb89f4573b4604dda4b37051d1dacfce16a7bbc69`  
		Last Modified: Fri, 02 Feb 2024 23:54:24 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df31e70de23926132574306825edfe7c11196d93bc0d61634ff9058cadb30c35`  
		Last Modified: Fri, 02 Feb 2024 23:54:23 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8b656557639abda7c2305bbad2f21046bc90d6243397872b0280db9b864894`  
		Last Modified: Fri, 02 Feb 2024 23:54:24 GMT  
		Size: 66.6 KB (66601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e351629a4343ffc7dcea51111fbd376c42f008234b2a2e17d003cc2c0d60ba`  
		Last Modified: Fri, 02 Feb 2024 23:54:22 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866138b28cc0f7c44f3c8865b26bfb4f62407509bc81112db04a4029b7e98b1a`  
		Last Modified: Fri, 02 Feb 2024 23:54:22 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2cc66c59e171f7a77f6bb6417b25e29b04ff8a53748b50b2d082b2bd8ad14c`  
		Last Modified: Fri, 02 Feb 2024 23:54:33 GMT  
		Size: 197.5 MB (197520670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0122cd184bbec3d6950b9126af255810bd02e1d63e05c358abbc20c6f53fec3`  
		Last Modified: Fri, 02 Feb 2024 23:54:23 GMT  
		Size: 3.8 MB (3828680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a1bf750e7b43c99c139af13c06db624116c2a94ca86a679a843f4ce4dd4f72`  
		Last Modified: Fri, 02 Feb 2024 23:54:22 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
