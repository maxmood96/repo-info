## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ddb4ddc26fa2754c1e577726bc22ab0e6b33612daa823b18f93b10f7df5193d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.2894; amd64

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

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:f733bd0b1682be3e5ca869346d32aff9c6378e2328601d2a37ffa07ad6678773
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195961533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465013bb7397ee88055117734d7d2077759204e7979f712e6fc9082206e9061b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 02:11:09 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:10 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 02:11:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 31 Jan 2025 02:11:13 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:11:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:11:20 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:11:23 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Fri, 31 Jan 2025 02:11:26 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0cc82873365f2feabbb386b072fb8175769ab45797a02f74e35c58599e3da5`  
		Last Modified: Fri, 31 Jan 2025 02:11:32 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381fa43710e9b81837a823850a4f28cc1741bae8272819b386dd12d849876eaa`  
		Last Modified: Fri, 31 Jan 2025 02:11:32 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ffd69b6a04457b467cb16e44461157ca2aa3db1c72207925e0c64fd529680`  
		Last Modified: Fri, 31 Jan 2025 02:11:32 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e47ea8fc74b803fed9050e49e65e653897d77ec6bb52a470b080f3dff6f36f`  
		Last Modified: Fri, 31 Jan 2025 02:11:30 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2a41a22817a98152a21312012cdba5dcde76626d98372ff5c84872c738a240`  
		Last Modified: Fri, 31 Jan 2025 02:11:30 GMT  
		Size: 68.6 KB (68605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b60705ff134a52697d46aeab5cfda4b5a36d5d403b0a6e6c6131b7f79c219e3`  
		Last Modified: Fri, 31 Jan 2025 02:11:30 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7b0c7ee76e9b7f306cd4d02f62c949554ec166655c90f6c826038a8e9e2368`  
		Last Modified: Fri, 31 Jan 2025 02:11:34 GMT  
		Size: 40.6 MB (40552229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77db9ef61f989864f4962dae4334eaccc8fbc25bcce4af1cdb5d64435bf89774`  
		Last Modified: Fri, 31 Jan 2025 02:11:30 GMT  
		Size: 68.0 KB (67965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
