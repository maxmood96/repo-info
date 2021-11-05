## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:6145969c6fa80aa2461966f5b9949ea5e8c423f0de06d8d21cdf93dfbb986491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull eclipse-temurin@sha256:e49e432f774e37bed7873894dcb20db92681e95642cb56a21b7c07052a22080d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291340741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e5e9ae8ad235eb192ee2210ff40221be85c1678ec1d4f0fb752ff4f2b51a89`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 18:17:55 GMT
SHELL [cmd /s /c]
# Fri, 05 Nov 2021 19:38:59 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 05 Nov 2021 19:39:00 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 05 Nov 2021 19:39:01 GMT
USER ContainerAdministrator
# Fri, 05 Nov 2021 19:39:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 05 Nov 2021 19:39:14 GMT
USER ContainerUser
# Fri, 05 Nov 2021 19:39:30 GMT
COPY dir:75727e79a870c9066772bd3811959a8f3c491ac4b54ae3b2c145d1638b6bc93f in C:\openjdk-17 
# Fri, 05 Nov 2021 19:39:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 Nov 2021 19:39:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ceff24c3c0c2c360cd3788fcde5c41e1d6601339f4944623c732558a6030e631`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820567e8abe8e66f7827d153f12db50a2d5e9b8dcc4da1de09945f0adbe3c82a`  
		Last Modified: Fri, 05 Nov 2021 20:38:01 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68442174a1a55c26dd2ac143bf99441efe66ef0f4d6d4692b22554797b0a639d`  
		Last Modified: Fri, 05 Nov 2021 20:38:02 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a97b5bef91a3b9db76238fd5e753aae033a4cb507a08a9fd4a71450d0cd4be`  
		Last Modified: Fri, 05 Nov 2021 20:38:01 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9351bcfb62b5b7e779fbc7a6606386b62bc8e18eb0d84b5a80ab3879210705`  
		Last Modified: Fri, 05 Nov 2021 20:37:59 GMT  
		Size: 70.0 KB (70038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e2c3d5681a46d19dd05671436468a3ec9fee2448bfe88de22d43bcd9039237`  
		Last Modified: Fri, 05 Nov 2021 20:37:59 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d36e03e6334585dbad33bdb20ae1061a1361513ec4a17c9ebfbcbc9918ef0fb`  
		Last Modified: Fri, 05 Nov 2021 20:38:18 GMT  
		Size: 185.0 MB (184950840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffc06280c56405e694c9ba2b11827a86e778ef3fe510a21f0d3c19644496f4e`  
		Last Modified: Fri, 05 Nov 2021 20:38:00 GMT  
		Size: 3.7 MB (3651706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffb3508b4c1fba3b8898ced0dddca151b228061385e0883fdcb7f00a92b7fe`  
		Last Modified: Fri, 05 Nov 2021 20:37:59 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
