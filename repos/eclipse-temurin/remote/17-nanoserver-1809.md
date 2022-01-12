## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:670f1062ca432887c3dbd82219c3b02072e240241e8f944552bc461e8a299b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull eclipse-temurin@sha256:270f57b8fe099fabe9b0a375da510bee854654ea6ddd2a802bbf07fd3ada76a2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291687829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd434be2aa83706529d958c5cd41719e253c3f713e3a414703e01a3cd92760f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:33:30 GMT
SHELL [cmd /s /c]
# Tue, 11 Jan 2022 22:16:07 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Tue, 11 Jan 2022 22:16:08 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 11 Jan 2022 22:16:08 GMT
USER ContainerAdministrator
# Tue, 11 Jan 2022 22:16:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Jan 2022 22:16:26 GMT
USER ContainerUser
# Tue, 11 Jan 2022 22:17:00 GMT
COPY dir:75727e79a870c9066772bd3811959a8f3c491ac4b54ae3b2c145d1638b6bc93f in C:\openjdk-17 
# Tue, 11 Jan 2022 22:17:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Jan 2022 22:17:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6cc5785ab09c66739c3205c3a26410f1cf4bf85c377fa81b240e754cf0659c58`  
		Last Modified: Tue, 11 Jan 2022 22:44:40 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7bafbaafb473c19a780298470b47c981eb427487ec11fec6a0513803ed1e8d`  
		Last Modified: Tue, 11 Jan 2022 23:11:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146d7ba2e72925e70b8cb5cccc9fb11d30eb5c1e63c658821294917083d8a6eb`  
		Last Modified: Tue, 11 Jan 2022 23:11:20 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca136dfbf1765c8e4fdc8d38a93bff7f7dc87cc920ff3f7861d65b4a8f77f7d`  
		Last Modified: Tue, 11 Jan 2022 23:11:19 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6347e4c3ded29f3f1dca92bf17130fbc95b9b38853681437e1cc0998f7d659ce`  
		Last Modified: Tue, 11 Jan 2022 23:11:17 GMT  
		Size: 70.6 KB (70561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024e3cc8e0edecdaa83890b60538167cdd56c94f6a5021f6281fcb90f0d6268c`  
		Last Modified: Tue, 11 Jan 2022 23:11:17 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314e53b03473328dc00d12aabcb22b3a1a9856c4af8c606cf8897bc125ed95a4`  
		Last Modified: Tue, 11 Jan 2022 23:11:38 GMT  
		Size: 185.0 MB (184951028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb257c077f3ee03bbb7cf9bf93c9a45180d1d81ba373edcad89d99984a3007a`  
		Last Modified: Tue, 11 Jan 2022 23:11:19 GMT  
		Size: 3.6 MB (3644866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185c429f9211e95c61e2ce8a15134632d48786b38137a889bea3d3f1b86d8527`  
		Last Modified: Tue, 11 Jan 2022 23:11:17 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
