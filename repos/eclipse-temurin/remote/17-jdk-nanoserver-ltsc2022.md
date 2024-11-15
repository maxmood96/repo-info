## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:4db8906cc2c28214c4f54a7e53cf7c582cd1f481b98bf8aedc207d94cb985290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2849; amd64

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
