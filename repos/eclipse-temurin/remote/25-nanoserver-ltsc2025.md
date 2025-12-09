## `eclipse-temurin:25-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:304545c32a2479c259326bad480cd667ffa5857f07c78c099bf906c720c28dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `eclipse-temurin:25-nanoserver-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:4f54c3ad12d5ab83041b963e6c37db0f436db6be7b1ff3ac9ac3ee8e43deb5d1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (337022484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f344e0bc22ca7ae716ced8148d05328f5f27464481bfb905816c2689ca3d990a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 21:12:53 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:15:50 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Tue, 09 Dec 2025 21:15:50 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 09 Dec 2025 21:15:51 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:15:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:15:53 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:16:13 GMT
COPY dir:889642903e29f32ff0f0b6da5f64cf6a40ecfa6d85d0926e4981ccbc885ac0c0 in C:\openjdk-25 
# Tue, 09 Dec 2025 21:16:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Dec 2025 21:16:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3aa2fd9c43d5870304ea449c22f4fbf73f16c064a13e04297c92a2a200461b`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d15d04145e59abb526d49bbdd03c5dbd6ce33aa8a73723d1e27a9d939039c4a`  
		Last Modified: Tue, 09 Dec 2025 21:16:41 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dc240b30e86d2534700429dade2dca3888b67c1ac97bd569db2d93de03380a`  
		Last Modified: Tue, 09 Dec 2025 21:16:41 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f7a622d99e8bd05777355dead0e94e3d939e139d98760a89f1cc5ac3cf4880`  
		Last Modified: Tue, 09 Dec 2025 21:16:41 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223e20f45fb92ca6bfabdbe35f3ac6c5bcbb9d2178860bb62325dcf274e375bc`  
		Last Modified: Tue, 09 Dec 2025 21:16:41 GMT  
		Size: 72.4 KB (72435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148cbadc722d7a523cf4d7db166b944c7bb5336382142ad2f55b88f6d440b2f7`  
		Last Modified: Tue, 09 Dec 2025 21:16:41 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d77443c121f6490ecebb6fc863ddbadf0e990cf9e81347e51dcf32fd7493be`  
		Last Modified: Tue, 09 Dec 2025 22:17:20 GMT  
		Size: 138.0 MB (137951773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc7b89a4bf412bbbaa530c8237f4a59288f4c065674d3a51cea61f3159d96ef`  
		Last Modified: Tue, 09 Dec 2025 21:16:41 GMT  
		Size: 118.0 KB (117965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3ee3875f6440eef3cf8ed65c92647cd4755a49683e8a86e4502a7946f8c1ed`  
		Last Modified: Tue, 09 Dec 2025 21:16:41 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
