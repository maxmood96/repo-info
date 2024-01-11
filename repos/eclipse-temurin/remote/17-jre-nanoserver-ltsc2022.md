## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:55aade8efa2ff0815bc5fa0b01b509e6e4604aab629a6ebeb931497ef6ac68d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:cd282ec1b5c41a2d0ae849a522bec0b8591e00354abe1fccf8e5420f6f3cf073
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164312445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a144b5d0f70490bd5bd79ed1ab289850c2e317a2954acccb5e74ddac4e8d0e4e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 23:19:42 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Wed, 10 Jan 2024 23:19:43 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Jan 2024 23:19:43 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:19:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 23:19:54 GMT
USER ContainerUser
# Wed, 10 Jan 2024 23:20:42 GMT
COPY dir:d3f692ac99669197443250e31cbc5c2f5282787fd78589cc9b6c2e91236738f4 in C:\openjdk-17 
# Wed, 10 Jan 2024 23:20:55 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:f8c0b41288d7a6dced95afaf6fe69fa8a0000dcbaff56e7f1d3e657e9cbd1f86`  
		Last Modified: Thu, 11 Jan 2024 04:20:26 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19ed1b114465c6285c07cee424dc0d2055f2f9ed3913a91e2fe3d894c95f2b7`  
		Last Modified: Thu, 11 Jan 2024 04:20:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1c7551f930b96326abc7cf55564fe9b20ec482df7c62f1c0bc253821fa5743`  
		Last Modified: Thu, 11 Jan 2024 04:20:25 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7608281d9daf7abcac939cb214476ed7b9bd942966d5f628325d372897231377`  
		Last Modified: Thu, 11 Jan 2024 04:20:24 GMT  
		Size: 78.9 KB (78947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee63e6da855b22ed10f2c0442e956225dfa84e60b8fe618ef5e840169cf85551`  
		Last Modified: Thu, 11 Jan 2024 04:20:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96dbbb9ad35c6773f8d9b185e3335e1ed794d04ae5cff4c4a4e2840817cbd546`  
		Last Modified: Thu, 11 Jan 2024 04:21:04 GMT  
		Size: 43.4 MB (43397411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06079dbeb2509110abc6425778fc2f9e0e8f563a20ebcdced5c7f843d5c1253e`  
		Last Modified: Thu, 11 Jan 2024 04:20:56 GMT  
		Size: 61.0 KB (61014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
