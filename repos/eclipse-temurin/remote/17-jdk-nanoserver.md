## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:f9047e2bb6d34c3cf053b85afe0c2bd4022a66acf546322a3dd63bf7d29aa6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:373c412ec8d734a1ca811744e65be7858dffb9fc0e99f2e800e9f06385bbe47c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.1 MB (309097096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983e9222e336ce7b2ece319e85cb7a60fb9ac598207e046a07ce7b78b8fba1fd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 21:16:07 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:16:07 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 14 Nov 2024 21:16:08 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 14 Nov 2024 21:16:08 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:16:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:16:11 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:16:18 GMT
COPY dir:52d780064906626480ed3e0e10c20681fda9fbf2926de2858bcee46524c2c3aa in C:\openjdk-17 
# Thu, 14 Nov 2024 21:16:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 14 Nov 2024 21:16:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d2cba0be2ad8b6822450d1f8d209d925b615eda1b8290c4c94b0a9f698896d`  
		Last Modified: Thu, 14 Nov 2024 21:16:30 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c35925935c7a577cb600961a60686600ae82c25d59c430cfa6f9e0189627aa`  
		Last Modified: Thu, 14 Nov 2024 21:16:30 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e1e0cc25174b19cba818d65955fcf5c9ccc21848019405bc39b51e455e88b9`  
		Last Modified: Thu, 14 Nov 2024 21:16:30 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69642871401a7e50ecbce4e788919cb4f001ab8c41e407e6369700a9054291b`  
		Last Modified: Thu, 14 Nov 2024 21:16:30 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fb1285af24e5d2ecb1da9a6ecee84e28a4e4eb2e32452ab4cf3b7a306e78b2`  
		Last Modified: Thu, 14 Nov 2024 21:16:28 GMT  
		Size: 76.9 KB (76901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b9bbbf6597d386e1c3a58755b9dcffc2a9ca9aa3971668b32768cf42614d47`  
		Last Modified: Thu, 14 Nov 2024 21:16:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11908bb06581357c5f516c3497511f5536ff225d8fe7f5a987107120afc15bd`  
		Last Modified: Thu, 14 Nov 2024 21:16:39 GMT  
		Size: 188.3 MB (188302374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f427cc794f394c97ee027a6893d9502ad40ce1dd1b37a85fc32977182789c4f`  
		Last Modified: Thu, 14 Nov 2024 21:16:28 GMT  
		Size: 106.7 KB (106697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1e6d5bf13ab3a4018d9745ae4a94af625aea7819038a264f65f04664aee95a`  
		Last Modified: Thu, 14 Nov 2024 21:16:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:c3b8959ce445b67f09eafc5dc2435e6465a68b8dc1a596065b619e7b814c6efb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347251507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c85e71f8387daab00314c32c071b28364a798f77931e7fa3c397ef62cdf8140`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:16:19 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:16:21 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 14 Nov 2024 21:16:21 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 14 Nov 2024 21:16:22 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:16:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:16:26 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:16:32 GMT
COPY dir:52d780064906626480ed3e0e10c20681fda9fbf2926de2858bcee46524c2c3aa in C:\openjdk-17 
# Thu, 14 Nov 2024 21:16:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 14 Nov 2024 21:16:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47601bd501a25563881d0f02a37dfdb45f0007c9ff30ace4a7bf434e0e7355d7`  
		Last Modified: Thu, 14 Nov 2024 21:16:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fdfd8313db2c9c14185c035e884db36f56608f7153bbb88a84b0f2b2ee083b`  
		Last Modified: Thu, 14 Nov 2024 21:16:45 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2858671f82055a4daa816c0dea824031055f30958f63a7cf800eb2145eec906d`  
		Last Modified: Thu, 14 Nov 2024 21:16:44 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053ba91e4fd6add510adce72052bda6af7565c7a30cafa13fe17cc631b49189c`  
		Last Modified: Thu, 14 Nov 2024 21:16:44 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e38a164d4b27de951e2addf1e356e0dc9b36be8699f5b01661e13395a47f24d`  
		Last Modified: Thu, 14 Nov 2024 21:16:43 GMT  
		Size: 84.1 KB (84104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be167152a420bff596339ad91c310a455312f8d21327cb78ce8389a2bb0dd07`  
		Last Modified: Thu, 14 Nov 2024 21:16:43 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8596a3e0b698972c2b87328a5ba54f7b77fe64c3651103b55d8173c257c0a38`  
		Last Modified: Thu, 14 Nov 2024 21:16:53 GMT  
		Size: 188.3 MB (188302719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba9675ecfc67541688a448caa555e1459ff0f0ced131472090bcf828c887cff`  
		Last Modified: Thu, 14 Nov 2024 21:16:43 GMT  
		Size: 3.6 MB (3644225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53c5308392afe06da0310e689c5de862f807b6b414646f116fe8ba940a3e09d`  
		Last Modified: Thu, 14 Nov 2024 21:16:43 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
