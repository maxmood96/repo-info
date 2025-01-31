## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:3cf0eff66b3fcd28101061db92879845b8290e35e484545532ee86382995c4f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:fff3ece08e0bc0313350d8a86893b986f0447836035590b241771308449d051f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239779814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644ac859b645534bd6ee1536ffaaf14ede567b4762552f84b8468bed3e1d9bca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 02:16:06 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:16:07 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 02:16:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 31 Jan 2025 02:16:08 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:16:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:16:11 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:16:13 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Fri, 31 Jan 2025 02:16:17 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e18aaaba21900fda6be6c17b5c73d14278d428a5cef7222d29b71512643a11`  
		Last Modified: Fri, 31 Jan 2025 02:16:22 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d73dc6219a18423baeba086785c8a8b34519f68f536908f760faeb64e9e1bb`  
		Last Modified: Fri, 31 Jan 2025 02:16:22 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bb639470168fae80ae42cfbda4d5c9a506c526c4854b0f03384842a36afd60`  
		Last Modified: Fri, 31 Jan 2025 02:16:22 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79705faf4c823a29e65c9b9590c9c056485d00cb49039e35ef7f2a475f64b761`  
		Last Modified: Fri, 31 Jan 2025 02:16:21 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5a7bb71a330115e8fc09284d1b77e800a734386e9fa96a32d3f2e953182b67`  
		Last Modified: Fri, 31 Jan 2025 02:16:20 GMT  
		Size: 75.9 KB (75914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14420fc3e063fdbab84fd2bc73cb3ff083cd8405d69224f484b77e71f4f2c643`  
		Last Modified: Fri, 31 Jan 2025 02:16:20 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d2cedb2a384184645631c4c8a6222806ebe0324d1dbd0331bc72b151504f60`  
		Last Modified: Fri, 31 Jan 2025 02:16:24 GMT  
		Size: 40.6 MB (40552463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3a7e4f25afed28d76593aca0c96a8994ccd0ad67b99ededcfcb2340c4f31f4`  
		Last Modified: Fri, 31 Jan 2025 02:16:21 GMT  
		Size: 91.9 KB (91942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
