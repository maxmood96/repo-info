## `eclipse-temurin:20-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:443544bdbe0f8bccf318730cf8db84458fcf3ba565f8be43ff3cdb1f1a0bbcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:20-jre-nanoserver-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:95296c7e5b7f398949ca886d3cff6576dd4dcf16be15b12ef7d13c6d49fa3d55
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153381819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3a9293a3d52c30072c233bb1c9086396f118fc83c80b52af10a63a962eb499`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 21:36:32 GMT
SHELL [cmd /s /c]
# Thu, 13 Jul 2023 22:05:42 GMT
ENV JAVA_VERSION=jdk-20.0.1+9
# Thu, 13 Jul 2023 22:05:43 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 13 Jul 2023 22:05:43 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 22:05:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Jul 2023 22:05:54 GMT
USER ContainerUser
# Thu, 13 Jul 2023 22:10:33 GMT
COPY dir:db4e97c4fd2cfe51abaeb1dfe2097f2044faeb2be3c3c04299b9c20e07c77033 in C:\openjdk-20 
# Thu, 13 Jul 2023 22:10:44 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13c473988daf5951866dd9b290bd6417227c1d7df6e811cfe11438d033a1eba`  
		Last Modified: Thu, 13 Jul 2023 22:19:06 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d62bdbae50ea5107e96f223e58acf04a48c5a1026befc163b868fc431635844`  
		Last Modified: Thu, 13 Jul 2023 22:27:04 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f721c84b9ba4db8a041679302c91e162147f18ca3473fe31aaf1ce195f2b561`  
		Last Modified: Thu, 13 Jul 2023 22:27:04 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39db0679078c0ab19cb1d43aaba827ba9fc60421bd4da8150877c63745c0f9`  
		Last Modified: Thu, 13 Jul 2023 22:27:04 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09baeab2e9e0f9a703df99df66f102274cbd935494f12b4b140f5bffa5006215`  
		Last Modified: Thu, 13 Jul 2023 22:27:02 GMT  
		Size: 68.4 KB (68376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5aaebecb942512ab4f0d9f67a6dfe5688eed16185b0f9c8cc40d28f4514ab81`  
		Last Modified: Thu, 13 Jul 2023 22:27:02 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1dbf4d0252d677d1c67743d9f974ad83774a98731462bcdd71c14bf31a60f9`  
		Last Modified: Thu, 13 Jul 2023 22:28:24 GMT  
		Size: 45.8 MB (45765302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51afd51904e9695885fa76887b22f6aba67e1894baaa32554932a0ff9f58a62`  
		Last Modified: Thu, 13 Jul 2023 22:28:16 GMT  
		Size: 3.1 MB (3134149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
