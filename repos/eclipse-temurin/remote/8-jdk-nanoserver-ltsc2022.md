## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d2dcaf930e093e8e0039c25776bd19d84d6c94cb7c51f1780a68a11031bd4d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:3fc60150a00671c00d4d817a6d17f922dc35204af28b6a1488b163dd27e674dc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225350578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9981e0d4924fa770500b61003de9fde2c6c36712917e0ad16740be5551d1e83`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:34 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:18:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Wed, 10 Sep 2025 22:18:34 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Sep 2025 22:18:35 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:18:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:18:40 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:18:50 GMT
COPY dir:184da149c84a7d26eb59eea9818ea043a400cd17024f2fafd00950f1891aab87 in C:\openjdk-8 
# Wed, 10 Sep 2025 22:18:54 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e0ce028103081865bc14b1610899edd5f6a839fc9d1f091fb2e07888198fc6`  
		Last Modified: Wed, 10 Sep 2025 22:19:41 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8008a54e5706b6ce47d30dfbb11107fdf8c6fda68e3c91dfe900fc0c4632b5c`  
		Last Modified: Wed, 10 Sep 2025 22:19:42 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70197f57fc7d7089443786b5e71fe6f53727e462f017b4ab4111b8669a919f06`  
		Last Modified: Wed, 10 Sep 2025 22:19:42 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2e32fdbd55db30113ce18135b8ac491fb930131b4b77a1355a3021bce50e29`  
		Last Modified: Wed, 10 Sep 2025 22:19:42 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bce1e9d808414b90d6321a888c5071d3b358fef782b1aa15fcb7dbc8658e73a`  
		Last Modified: Wed, 10 Sep 2025 22:19:42 GMT  
		Size: 75.6 KB (75617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb26c3f451bbdb92a44be05e0677f23323779e9ee00d4cc3265bcac6ab05abbd`  
		Last Modified: Wed, 10 Sep 2025 22:19:42 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea5f94a5ef5240ce89052827061c34f11d96696a918fcf86c15641e61c73b8b`  
		Last Modified: Wed, 10 Sep 2025 22:20:01 GMT  
		Size: 102.4 MB (102434623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776dfb1f7f55e3233545e89973662cd962802a1d458a152a0bc4b415ae856f50`  
		Last Modified: Wed, 10 Sep 2025 22:19:43 GMT  
		Size: 115.0 KB (115035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
