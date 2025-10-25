## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8bf70c9522bad401fd5e381aebf773b15d8c27661f07e14d9e68fd58ba0abf60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:094283d450ac67dc69afe905e43d07660dbaabecf2c0ffb18d42b3015635682c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296643320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253ffd65e19a7bb4696edec4e6ef6878747e419d5f37eb00db88d0e4adabca84`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 19:18:10 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:18:10 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 24 Oct 2025 19:18:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 24 Oct 2025 19:18:11 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:18:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:18:17 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:18:27 GMT
COPY dir:184da149c84a7d26eb59eea9818ea043a400cd17024f2fafd00950f1891aab87 in C:\openjdk-8 
# Fri, 24 Oct 2025 19:18:32 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83cebb83f6b313d71f35f2d1a02bbae815244e3a733c544d5d2c4f807244e09`  
		Last Modified: Fri, 24 Oct 2025 19:19:32 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37813ab7778d16cb75a64091faa37ad39286c17dbccf955d662e04a2308640bf`  
		Last Modified: Fri, 24 Oct 2025 19:19:32 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87ec9cb17636b02e358730fa8c364b5d35804df80f85e64e15c5e5ee7168406`  
		Last Modified: Fri, 24 Oct 2025 19:19:32 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e2009d725a723299d8663565b0abbf02649886314d40ff0c55d865b60534f1`  
		Last Modified: Fri, 24 Oct 2025 19:19:32 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d28d59e62bed6e182dff0e4ccbccd026e4c4ad69cdd3a88c0c2f4b1013d49a`  
		Last Modified: Fri, 24 Oct 2025 19:19:32 GMT  
		Size: 70.7 KB (70679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebf1f884188794a882d84138a09bf4d671faf458b9558fd5210a11587fcf0f9`  
		Last Modified: Fri, 24 Oct 2025 19:19:32 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb30428102123532a237f933a95838c4815ba2270b7a4305418cc676adc9759e`  
		Last Modified: Fri, 24 Oct 2025 19:19:47 GMT  
		Size: 102.4 MB (102434828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06deeecf07ba682e29799b7dd6203322a82a24d16516af4be94d946552d9e29`  
		Last Modified: Fri, 24 Oct 2025 19:19:32 GMT  
		Size: 103.1 KB (103063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.4297; amd64

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
