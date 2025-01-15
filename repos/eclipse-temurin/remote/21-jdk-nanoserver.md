## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ea68ae84fbfeba3a77dcbe2a7ff9a6ec4426883d954ac2b31ab2d5ed28ea6a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:aa0ecc64d163c2e096febfc8d62efc759ea54475c8b26bba6e33929ccffdf87d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323428991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d433eb0603906cb500451182f7f121e90d4b4ddded570d78f72ee9f7dd738f3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:03:50 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:03:51 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 15 Jan 2025 18:03:52 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 Jan 2025 18:03:52 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:03:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:03:55 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:04:02 GMT
COPY dir:cc909cc6d9328a16dd1468618a073abc368d41e200a32534756819e3433a0b04 in C:\openjdk-21 
# Wed, 15 Jan 2025 18:04:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jan 2025 18:04:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396c99d0aa317706c66b94d5c540590d514e7126261ee9233696fa2701de3b4`  
		Last Modified: Wed, 15 Jan 2025 18:04:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0f7dd8e71d0459702acc384f502eba5d97fa4496f654c1031f0f87030bb77a`  
		Last Modified: Wed, 15 Jan 2025 18:04:11 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e040b932910a377ac9f8a2cfce3996da68478d51303296fc1cd26890b9596f80`  
		Last Modified: Wed, 15 Jan 2025 18:04:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22e89e8a4b0e085a36a131f5b1999728304fdb5af41628e8097c5f6b64e42ee`  
		Last Modified: Wed, 15 Jan 2025 18:04:11 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d406ee34f8101211f624c423ec04c27359e3dbbf40ade69629caa9ad83421c`  
		Last Modified: Wed, 15 Jan 2025 18:04:10 GMT  
		Size: 78.7 KB (78669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f33156a3c636330d331451bf7b731cdc029043be60d540250ddcf3f04cce96`  
		Last Modified: Wed, 15 Jan 2025 18:04:10 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49916c855bda31956cf602ffb7df7833af32a1b1c5c03181073c5f2e7392b332`  
		Last Modified: Wed, 15 Jan 2025 18:04:21 GMT  
		Size: 202.6 MB (202575611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9890f46b2da0e27b50366f145b05cc82fe92266a47118fbac472df33271bae40`  
		Last Modified: Wed, 15 Jan 2025 18:04:10 GMT  
		Size: 107.0 KB (106971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631b9a9d46a269eee51df0bfdd9909d254f21b503d04358a8dca7dcf91892e37`  
		Last Modified: Wed, 15 Jan 2025 18:04:10 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:9c66a90c94a7ec59d554473769addb0abe24707fe254a2ed5fa43e2b995e5d27
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.8 MB (361781032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0238ae5ebea413223b4f0d8a40e62649a5b9e4043b42f9fee6a17c0c6ea3f88b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:56:08 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 17:56:09 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 15 Jan 2025 17:56:09 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 Jan 2025 17:56:10 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 17:56:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 17:56:12 GMT
USER ContainerUser
# Wed, 15 Jan 2025 17:56:20 GMT
COPY dir:cc909cc6d9328a16dd1468618a073abc368d41e200a32534756819e3433a0b04 in C:\openjdk-21 
# Wed, 15 Jan 2025 17:56:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jan 2025 17:56:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472c054a782d18b0eec06a9d110587d787d33eb60621c48a7e6e1d44ac872bd3`  
		Last Modified: Wed, 15 Jan 2025 17:56:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9396536740a2810a03a2caf9ee4d18793bed2af5d9e0a6e02da098a6cbce88d`  
		Last Modified: Wed, 15 Jan 2025 17:56:33 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f3ab3a47ed855572c1915dc6c246aa48935e0c3e5a599a1358945862a9228`  
		Last Modified: Wed, 15 Jan 2025 17:56:33 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e99af066cdf4b79f973c81406abc2dcc2e2499c36a6e1d270ce24b07d758348`  
		Last Modified: Wed, 15 Jan 2025 17:56:33 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ff746f8819e4267c5b98d1506edee0ce1a9bd012ba40c174457da38d61dbb3`  
		Last Modified: Wed, 15 Jan 2025 17:56:31 GMT  
		Size: 74.4 KB (74364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460a636e73aba318be3a5592d72ff53d6abb485f55d0839a3bdc5097fe8c8ffe`  
		Last Modified: Wed, 15 Jan 2025 17:56:31 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8d7f84391f96070a5652e44f009362b8bf27f4351d83941d572ddcada0f27e`  
		Last Modified: Wed, 15 Jan 2025 17:56:42 GMT  
		Size: 202.6 MB (202575720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd1091734843efeb1e8728939e14bb8f0f944f68c1264d82a9b09055a9631b9`  
		Last Modified: Wed, 15 Jan 2025 17:56:32 GMT  
		Size: 3.9 MB (3857142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b66d7daba179f012291f7b3d6a40563bc53a20927e1e10fbb287070400fb8b6`  
		Last Modified: Wed, 15 Jan 2025 17:56:31 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
