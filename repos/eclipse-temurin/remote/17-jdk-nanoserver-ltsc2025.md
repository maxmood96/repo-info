## `eclipse-temurin:17-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:64374f2fa9bce25315cb7ebd540e477f999e8cb7364420ce3904da1cb4ca6b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:0e9e4a9a5a1dd2f6f756ca873275c287f83cdd9fede15f33af144f086d40f5c2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.6 MB (377578276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dccc0de7967d0a5ecb3bd8493b1c01734987ade56f43ded80326288a0b6a95`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:14:04 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:14:06 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 18 Apr 2025 04:14:07 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 18 Apr 2025 04:14:08 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:14:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:14:12 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:14:20 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Fri, 18 Apr 2025 04:14:27 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:14:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32d382d416f9ec3df2407aae0e3ff4ad39a3418bf6e737b85fb223177183dc7`  
		Last Modified: Fri, 18 Apr 2025 04:14:34 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe52f2eaba454a8595e6a40d57364b6bda57a1e25cbb0d71bcc4402ea7c47fad`  
		Last Modified: Fri, 18 Apr 2025 04:14:34 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4a4dc7b84fea4b7f3ad66854cf22e4e8d068c8c20238231aea3cad7acc8be`  
		Last Modified: Fri, 18 Apr 2025 04:14:34 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9f7ffba209e4310fe43277bbd1d2aa9604573d4348a7ca100c73ee4dd53902`  
		Last Modified: Fri, 18 Apr 2025 04:14:34 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c0dd667e9d63f46b8e4af6810ad2617a613782d0ffc91ae19aa78678378625`  
		Last Modified: Fri, 18 Apr 2025 04:14:32 GMT  
		Size: 79.8 KB (79766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb95e8e268f36f8c2e95019e0cedffcafe81a863f5819ed97588e555abfac760`  
		Last Modified: Fri, 18 Apr 2025 04:14:32 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4633b01a84745feb93227552b648df2c2ed4fcac92caea647fcd789af4d218af`  
		Last Modified: Fri, 18 Apr 2025 04:14:42 GMT  
		Size: 187.2 MB (187235525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b3b3b3c57c7aaa376423d16efe07eb7684b881748a624c65275c4084b391ab`  
		Last Modified: Fri, 18 Apr 2025 04:14:32 GMT  
		Size: 114.7 KB (114656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced9c36fbdd3b9d9d6a3e3e568ff99dc8281b9c9f84945da8955a2fa7342c72`  
		Last Modified: Fri, 18 Apr 2025 04:14:32 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
