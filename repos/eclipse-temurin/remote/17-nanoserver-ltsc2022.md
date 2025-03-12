## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8141815a4b6d0f10d48c95d0ee92f1805f256a5badadd44c4691ef8006b4afde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:17155b3c0849868ba2bf899fad662235af09ba9975dccdf34301920e406ffa46
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308121580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b99f4c9b4046e49b8c8287049de87d0f9c4a8bf92d25937cc5092c888a77fb1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:18:38 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:18:39 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 19:18:40 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Mar 2025 19:18:41 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:18:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:18:44 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:18:51 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Wed, 12 Mar 2025 19:18:57 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:18:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b328139370a196fd32643d205d7cae2a59d0d0a767ebd444eb2ac8f36c3f6cce`  
		Last Modified: Wed, 12 Mar 2025 19:19:04 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed1bff0c8c0431d3fc37b1c454c9235cc57ca654efdfabb2fcf9d02699bca76`  
		Last Modified: Wed, 12 Mar 2025 19:19:04 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df91f22df2297ab58bd6db3381891731a5e6a674bd56753ef111cd89ecdcaf3d`  
		Last Modified: Wed, 12 Mar 2025 19:19:04 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74619840efd21987a2480a08cbd3a641231fd6794d2e0cbc0f078f9d99cd81be`  
		Last Modified: Wed, 12 Mar 2025 19:19:04 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57890ddf75c9c00498b54243a54f996f8be7d3fed807595ddc60eb54c1b7dc26`  
		Last Modified: Wed, 12 Mar 2025 19:19:02 GMT  
		Size: 78.8 KB (78773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366b8c090a41c7c11c4360f7f4e4da23982ee47a0b85fae5453ffc1aeeaf70b1`  
		Last Modified: Wed, 12 Mar 2025 19:19:02 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a928294aeb039a3bcb66660e12d52aa22a43dbbbdafaad25d4f4790aeb6248d7`  
		Last Modified: Wed, 12 Mar 2025 19:19:13 GMT  
		Size: 187.2 MB (187233811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a3b39c01ba6a8f97a37ab80eb9432a2ac14d3bebf9e3a2d7f69cdd677e97d4`  
		Last Modified: Wed, 12 Mar 2025 19:19:02 GMT  
		Size: 107.2 KB (107247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d21002906a9730ebba0223789b644b6738e517433d7a98daaea55e56780a44`  
		Last Modified: Wed, 12 Mar 2025 19:19:02 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
