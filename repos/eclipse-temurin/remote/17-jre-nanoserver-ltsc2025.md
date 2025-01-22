## `eclipse-temurin:17-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:12ddd1d61e5aac78345790ab88170b9c117303d2da6efb64f85fae56bd9c62ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:e6f34e4f5f5ef5a7cc95bd4e07e9eb4e699981b2f6af6f44c8763bde7b0ab1f2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243589784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0411f1f472ccdafba2ce37c218cb170177775a030a223eac1734d6a83bd76ae2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 19:34:51 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 19:34:51 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 22 Jan 2025 19:34:52 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 22 Jan 2025 19:34:52 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 19:34:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 22 Jan 2025 19:34:55 GMT
USER ContainerUser
# Wed, 22 Jan 2025 19:34:58 GMT
COPY dir:4c6d77ca6f58a330005c5f34389fe1882335ea3db28c021259e868cb18ddb756 in C:\openjdk-17 
# Wed, 22 Jan 2025 19:35:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b78dddccdfd1c5bca979d490a74657f7c8a335c7d959d2d4d6d6162962677d`  
		Last Modified: Wed, 22 Jan 2025 19:35:08 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab0ced27f16c90c37483792f0dfbca6111d9698d79f498b10f18db888eb8648`  
		Last Modified: Wed, 22 Jan 2025 19:35:08 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7992de6c0340d5660f17853566d43271b2631f48f26acdbd0b2da98ac3d74d`  
		Last Modified: Wed, 22 Jan 2025 19:35:08 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0d1e8b3c4d5e9a433c8ec373f100d57d0c658f22a568e636ad09a73dd428af`  
		Last Modified: Wed, 22 Jan 2025 19:35:06 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b0391991fc64cdc5d4b91ec6df9488808e408f3a0f78195529526366a5bd02`  
		Last Modified: Wed, 22 Jan 2025 19:35:06 GMT  
		Size: 77.3 KB (77307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b087bfc2de39ed5bc3ecf00860eb8e54debc0e6f370b410ba0445820afe2f7`  
		Last Modified: Wed, 22 Jan 2025 19:35:06 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b1e3fc7bca4797237a598685b23ba9779b9eb8dd25159396bd59e394d89cef`  
		Last Modified: Wed, 22 Jan 2025 19:35:12 GMT  
		Size: 44.4 MB (44360321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063ac545053ff0e5c106b57c20b518bc68d359cfe7c135bd11d3cd6a45e56aff`  
		Last Modified: Wed, 22 Jan 2025 19:35:06 GMT  
		Size: 92.6 KB (92600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
