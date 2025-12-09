## `eclipse-temurin:25-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4032d007cfe39600aa696ea89b7b796bb7b4e4e0fc41b9175c175cc0089b2b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:25-nanoserver` - windows version 10.0.26100.7462; amd64

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

### `eclipse-temurin:25-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:2fdbb70dd061d874fdf722b46630bf50874b6232a3f692a555b698348596e281
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264503706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0695ffceb12cdd193f8c7bb853fe8d7645013cd4e1b57826239294ccbece9535`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:46 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:13:22 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Tue, 09 Dec 2025 21:13:23 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 09 Dec 2025 21:13:23 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:13:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:13:25 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:14:15 GMT
COPY dir:889642903e29f32ff0f0b6da5f64cf6a40ecfa6d85d0926e4981ccbc885ac0c0 in C:\openjdk-25 
# Tue, 09 Dec 2025 21:14:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Dec 2025 21:14:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7870d3a44198dbb615532c3d59d7e87b8da8857e8ce6472008152cd114373be6`  
		Last Modified: Tue, 09 Dec 2025 21:13:11 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfca3db2b6d8c751de1c057e4cb9412f3b83f501541bb58b72f70aba8a6c4ce`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7303dab28fbf7a2c09b3870b5c863e7d1802c0d13b0aca1b8f5c0d699996b4f4`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2ef1d534905cb9cae1ba330997663b80067a86bbe5650ce5f659c721f46f3e`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0add70c3e99511a3a051355918450667dbb61b5422ba039b53d6d1ac97734240`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 78.8 KB (78812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea2015205d244c634b6776088b40787f607e621a090b6dfec798817b5c7b16a`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da774cc8f033ba5595553170e3f9ffa26468b3e40301fd676286fcceea32ea0`  
		Last Modified: Tue, 09 Dec 2025 22:17:22 GMT  
		Size: 138.0 MB (137951635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b36cbd30f9d7a60f4efe03e11c4909c5b952cde1cdb33c3951b6b0a5162fbfa`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5bb8ef7067a2b029799befd530769991b420e8122226af2eaaac038169d205`  
		Last Modified: Tue, 09 Dec 2025 21:14:46 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
