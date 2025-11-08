## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e7fcf00f782dacc510a179c47fb2b5c698d7da5c6789518ef6b78d4f97f7fb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:46b234427a9ee27f76bf5f36a2d843d1e6d183a43fffb121e855ed55928d6eb1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166552510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27f96b313281ca381ee3c36563dc4fa71527f05f131f55fd622aeca523ab6f5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 08 Nov 2025 18:23:37 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 18:23:38 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 18:23:38 GMT
ENV JAVA_HOME=C:\openjdk-11
# Sat, 08 Nov 2025 18:23:39 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 18:23:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 18:23:46 GMT
USER ContainerUser
# Sat, 08 Nov 2025 18:24:03 GMT
COPY dir:4835e564d5b678d207d3850b6f40a90e0afa12e9d665c48e7909a88923b1a7a8 in C:\openjdk-11 
# Sat, 08 Nov 2025 18:24:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dd552d57286aa4c7a7dccb4c72e0a1c4232c55ec6b6af0c902477b336d0513`  
		Last Modified: Sat, 08 Nov 2025 18:24:23 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644628c49bbc71543cfea90b8241fdc7489f90736a10f0e0b0c7588aa0d16cc5`  
		Last Modified: Sat, 08 Nov 2025 18:24:23 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd36052ec27bc71796cb778be6d91ddc1267bab580d306e4eb1caa638df9988`  
		Last Modified: Sat, 08 Nov 2025 18:24:23 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764bffb07e61e0413aee068504ed0328b0da11e66154920b03817ab49b0ffc4d`  
		Last Modified: Sat, 08 Nov 2025 18:24:23 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216f96599d8d142fcafa5132fc60e42848bf0895fa1b85f500f15f73d35beb35`  
		Last Modified: Sat, 08 Nov 2025 18:24:23 GMT  
		Size: 71.3 KB (71258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fd1a5923d600b3fc6e60f609873741a556632a9fdde5984ce43612208a16eb`  
		Last Modified: Sat, 08 Nov 2025 18:24:23 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092dd449896f6a40e429a316bf8c552b49565b516cc79ce0efac257e43dd0965`  
		Last Modified: Sat, 08 Nov 2025 18:24:26 GMT  
		Size: 43.7 MB (43695020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79186aef00af8c4c530cb172c2437dbd1b6ba06bd787a6d9ad5c4b80c96a851a`  
		Last Modified: Sat, 08 Nov 2025 18:24:23 GMT  
		Size: 96.9 KB (96860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
