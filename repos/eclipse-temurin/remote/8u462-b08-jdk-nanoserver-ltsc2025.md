## `eclipse-temurin:8u462-b08-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0dc58ec7881d438a8a0f29d4208c0298bfcbd341c209ae00a0606beede2f7a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:8u462-b08-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

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
