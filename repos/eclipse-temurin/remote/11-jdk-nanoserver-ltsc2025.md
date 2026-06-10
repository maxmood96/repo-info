## `eclipse-temurin:11-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:88b0923efac8c734e91d162f1fcbd74feaf0a766fc080708bc32df016515118b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:023fb4d156a424019e14890e64813cd5c38594620ca51fcd9d80b8b4db52ce36
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.6 MB (391645345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e30fc47e89191db64875cce13dfec069c462840a4e29e168423ce4f6bef36fc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:20:06 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:20:07 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 09 Jun 2026 23:20:08 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 09 Jun 2026 23:20:09 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:20:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:20:15 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:20:33 GMT
COPY dir:508f69ae524938b28a83a19a9aeade10facf00325b620c7a836698644d966097 in C:\openjdk-11 
# Tue, 09 Jun 2026 23:20:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Jun 2026 23:20:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a4212199a2492ffd90053401f0671a7aad235421e10c6dd150b4603e354a1d`  
		Last Modified: Tue, 09 Jun 2026 23:20:46 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd59c64073169ce3c0225ffbc0bcf51171ee08fd8f24161b533bc2c7272e03d7`  
		Last Modified: Tue, 09 Jun 2026 23:20:46 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5f6eb46fba3b53d7a67fdc6632b7debe97af5b05772c459b0ed7446a431a69`  
		Last Modified: Tue, 09 Jun 2026 23:20:46 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496fa56ea54486bd676b10216a921d894b2957163bd860ea581eb5ba65034ae`  
		Last Modified: Tue, 09 Jun 2026 23:20:46 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad10fc7d36ef88d3808cd8b1f587f70d705c27980c3844d477a4a1d43b1ce7c0`  
		Last Modified: Tue, 09 Jun 2026 23:20:44 GMT  
		Size: 70.3 KB (70328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dc184086f8be3865aa32e99e561f427065bcb7f091ca7172dd4c6cf3bf460c`  
		Last Modified: Tue, 09 Jun 2026 23:20:44 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103544395de904d741b0613cf0fd9e8e8e1967d315b7b9ac2a93479c4e3a2975`  
		Last Modified: Tue, 09 Jun 2026 23:20:57 GMT  
		Size: 194.8 MB (194786257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0064f7d0bb2bd427085ce116d69f7158d5d25a816ea3d84f20fc3cefb64a9501`  
		Last Modified: Tue, 09 Jun 2026 23:20:45 GMT  
		Size: 114.4 KB (114396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6185ae6a3d4143d193ca6dfe76a55c47150afdc647e5afa975ed4789db255bb5`  
		Last Modified: Tue, 09 Jun 2026 23:20:44 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
