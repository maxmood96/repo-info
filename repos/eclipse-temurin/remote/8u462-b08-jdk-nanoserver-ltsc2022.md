## `eclipse-temurin:8u462-b08-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8ffbeca74b6e3764e514729ac2a0dfb2d7155fd686c38f7a954b324b4b854ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:8u462-b08-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:520c4581520ef41ee839a1bd673a4fdb3cd5c1f1284a4fd8071155041201ae15
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225348110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9568d30de2784668a420ce8410dad9c0bd2548f4023c42026526eecb2645f064`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:19:18 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:19:18 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 24 Oct 2025 19:19:19 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 24 Oct 2025 19:19:20 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:19:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:19:23 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:19:44 GMT
COPY dir:184da149c84a7d26eb59eea9818ea043a400cd17024f2fafd00950f1891aab87 in C:\openjdk-8 
# Fri, 24 Oct 2025 19:19:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde8d3892490c03c6867f198f3dc45e69fe1049b2d63e6fc8a4a21f54095e87d`  
		Last Modified: Fri, 24 Oct 2025 19:20:16 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d245c487234e7bd232c9b081047b096be481102104daeb7d163c83228b5bc3b`  
		Last Modified: Fri, 24 Oct 2025 19:20:16 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a60a58403d4cecdd3c38bb7c99f468758749567bcd53feaecfd1d99c036c853`  
		Last Modified: Fri, 24 Oct 2025 19:20:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530ef0f40c2c944968fec11c55c2e4cb02c3d06438092b6d48c3edc08648c5a7`  
		Last Modified: Fri, 24 Oct 2025 19:20:17 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c954436aa948053c3ff187c066beffea2c43f95981549423a1948a27346832`  
		Last Modified: Fri, 24 Oct 2025 19:20:17 GMT  
		Size: 87.8 KB (87848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2ea8d571ec3f7b3dc40472dfb948e0038492e32707050f9801352a41f19d6d`  
		Last Modified: Fri, 24 Oct 2025 19:20:17 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e639c4ecd9829926f1e8f1dd9a98d376bb94171dc4292c07b9d744bc268ad490`  
		Last Modified: Fri, 24 Oct 2025 19:20:32 GMT  
		Size: 102.4 MB (102434445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ea67d9929b677fde622b5b0f4ae43ad7af93c05f8f2e1de2cc7e08ff8f79ed`  
		Last Modified: Fri, 24 Oct 2025 19:20:16 GMT  
		Size: 136.5 KB (136462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
