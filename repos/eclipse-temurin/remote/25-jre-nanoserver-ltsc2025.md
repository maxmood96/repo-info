## `eclipse-temurin:25-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0dc6fc75524b8dbe658e929d078403af3f25b2657607d2883a25a59ead3ebee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:fab9a7b5625c36b9d7fa66d858aab5a6bde3470bf116e508586e48eb89fa0bd0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258525346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7730066aee95107b08217b96315d1802213e65516acc3f89ec7bb29d4171734`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Fri, 01 May 2026 00:08:11 GMT
SHELL [cmd /s /c]
# Fri, 01 May 2026 00:08:12 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 01 May 2026 00:08:12 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 01 May 2026 00:08:13 GMT
USER ContainerAdministrator
# Fri, 01 May 2026 00:08:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 01 May 2026 00:08:24 GMT
USER ContainerUser
# Fri, 01 May 2026 00:08:44 GMT
COPY dir:fd8baea77fa86bd13952f69621f69e815eb87406af0c0441c94fb1b8a78482df in C:\openjdk-25 
# Fri, 01 May 2026 00:08:51 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4d9fe2483e9db65da858e1ae2ea02d1279f6c938b58044c81f8db4a04e5ad7`  
		Last Modified: Fri, 01 May 2026 00:08:57 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b42d8e59dc3481c564b4348af8d1ca8432bd6fce2c3623ee0fab93881ffe2e`  
		Last Modified: Fri, 01 May 2026 00:08:57 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ca9a9e90f3611e990e5c1a82d1c3e84dd97d8e64765738c7da3187518a5695`  
		Last Modified: Fri, 01 May 2026 00:08:57 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539c379cf38f5fc6fb34f6fa5ef50d24b06099a3506495596f4b8f9ca3a73b6e`  
		Last Modified: Fri, 01 May 2026 00:08:55 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9e6fb9583d7c536ed2003fe82ba0a49794d841df0fd120773121cb5fc25a50`  
		Last Modified: Fri, 01 May 2026 00:08:55 GMT  
		Size: 69.7 KB (69740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f31cba567d7be3adc8ad852283e67802bf3cba703851cce7084ff37bdfc5d3`  
		Last Modified: Fri, 01 May 2026 00:08:55 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7f7eab8ff0a860544b77115eb5c6904040e8dcdb00d6e7f9896ba3c1da1146`  
		Last Modified: Fri, 01 May 2026 00:09:05 GMT  
		Size: 58.6 MB (58619920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33a3ff329677096d01f02c676506df31a3000da9691edd029e73c77d400ed6a`  
		Last Modified: Fri, 01 May 2026 00:08:55 GMT  
		Size: 113.2 KB (113243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
