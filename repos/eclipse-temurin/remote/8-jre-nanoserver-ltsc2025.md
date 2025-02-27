## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0a47087eded4bb15cbb110772a683ed0f19b4031eba89226a6492500473351ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:0a9760279d9e4de578b510d865e20a1dcbad20dc993893f52fef0bc1454c4c17
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246622713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df3cfd2c1a44d7a05d575597272893395ee3ccd2933066477e52a98bcdb8573`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:14:02 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:14:03 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 27 Feb 2025 19:14:04 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 27 Feb 2025 19:14:05 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:14:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 27 Feb 2025 19:14:10 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:14:13 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Thu, 27 Feb 2025 19:14:17 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf8c648f739270cc2cbaae9f0909358ad182d7408cfe5decacb0f3235216b50`  
		Last Modified: Thu, 27 Feb 2025 19:14:21 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767a636b0d34cb71d72fbb4ef0f8b16edb3e3ea1519a7111dfe0ecfc2e606851`  
		Last Modified: Thu, 27 Feb 2025 19:14:20 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567eb05e3c9d20cd7aa03dddf65f55a004c71068dec72e04dd8395125aa32c3`  
		Last Modified: Thu, 27 Feb 2025 19:14:20 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe0d360ba227b9d5fce16fae65d0d49acdf76107ee70ed564bafbf3c8a200f3`  
		Last Modified: Thu, 27 Feb 2025 19:14:19 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e342002a38b4183fd1703890ecdd5730b7022fd70535dd61c7b7482834e91e01`  
		Last Modified: Thu, 27 Feb 2025 19:14:20 GMT  
		Size: 78.6 KB (78624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945173c9742068ea655314705d66877e52ea2edc577f3ffc859873ffcb7ff448`  
		Last Modified: Thu, 27 Feb 2025 19:14:19 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499abd2063611c8b13e6574ee0b4a6214ba83b523721453b34fc3dc5a223f110`  
		Last Modified: Thu, 27 Feb 2025 19:14:23 GMT  
		Size: 40.6 MB (40552486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d48bd5633f050a7157f7e0d7bb6efd5980d79c625153ce16a50991411d1d00`  
		Last Modified: Thu, 27 Feb 2025 19:14:19 GMT  
		Size: 96.1 KB (96083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
