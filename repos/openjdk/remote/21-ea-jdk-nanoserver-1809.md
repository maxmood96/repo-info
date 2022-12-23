## `openjdk:21-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:a6dc87e654e267fc02f7e1a520de1875f2b1cc41eeaff60841bd9a5f5c9895d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `openjdk:21-ea-jdk-nanoserver-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull openjdk@sha256:aa56f3d0b58a9bd752c0fa7029e95d99216c1f54a86ff7eba3703b606346cf2a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304454271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a89ac33868fdf78e889595ffbd31f6c6471c7c138a80a0743d6b7dbde31f1c1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Tue, 13 Dec 2022 22:53:34 GMT
SHELL [cmd /s /c]
# Wed, 14 Dec 2022 02:56:32 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 Dec 2022 02:56:33 GMT
USER ContainerAdministrator
# Wed, 14 Dec 2022 02:57:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Dec 2022 02:57:30 GMT
USER ContainerUser
# Fri, 23 Dec 2022 01:20:50 GMT
ENV JAVA_VERSION=21-ea+3
# Fri, 23 Dec 2022 01:21:10 GMT
COPY dir:a0b3c40c87939552a74cb47bcf27e5d8bcdeff0ec0a12ada6354ac01531cf4f5 in C:\openjdk-21 
# Fri, 23 Dec 2022 01:21:54 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 23 Dec 2022 01:21:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fe06cbef5ac46e54edd743daf1bc2bfa36b294c7ce9104837061c41a4bde7b`  
		Last Modified: Tue, 13 Dec 2022 23:57:01 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f403eb4656dcd257924d61f24cde07e6a0bd4ea52ceb2fbb6aabbe94c2b76b67`  
		Last Modified: Wed, 14 Dec 2022 08:47:11 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfa39493326e86ec6b2f2fd8125ad183b1ed64b2c3f2a4461f05d827cc0926a`  
		Last Modified: Wed, 14 Dec 2022 08:47:11 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b7523c236c3ef82ccdd5905f89f123933015a7d581e70a248676aa7e3a76df`  
		Last Modified: Wed, 14 Dec 2022 08:47:11 GMT  
		Size: 66.3 KB (66297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063f4c761ac43a960d04eea23db92193fd5460a992bd8ac71186731abb9de13c`  
		Last Modified: Wed, 14 Dec 2022 08:47:09 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edb0782cc61ad72141eba684483175b3dd223f9a0bf38516257176baaa0bf60`  
		Last Modified: Fri, 23 Dec 2022 02:20:59 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5dd0418124b6fe27aa359141f4bed09151902ce36168ad54336bca98f04679`  
		Last Modified: Fri, 23 Dec 2022 02:21:26 GMT  
		Size: 193.9 MB (193946611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f577fe06dd09ab7d78118fded46a40b5b5005fe4d5aa8fcb1f6206d983ce98f4`  
		Last Modified: Fri, 23 Dec 2022 02:21:01 GMT  
		Size: 3.8 MB (3763363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf843542c42baffd6eea6ef2f876d80298ad192033c5a8fcfb1dbd096bc6f72`  
		Last Modified: Fri, 23 Dec 2022 02:20:59 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
