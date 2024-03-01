## `openjdk:23-ea-12-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:c2f1129d1b68bc3c0f9bd92f433a9a1db1afe069066e8e11f00f4aef421cde99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:23-ea-12-jdk-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:513a77c42e02a43cce1c6bd095b8fa70c2a27bcdc818efae9f1f2991cda25c0a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306071320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af200722d4b17e06f65224116c5a6ef976ae8a1a78316432b550867076d95bbd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Thu, 29 Feb 2024 23:50:45 GMT
SHELL [cmd /s /c]
# Thu, 29 Feb 2024 23:50:47 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 29 Feb 2024 23:50:48 GMT
USER ContainerAdministrator
# Thu, 29 Feb 2024 23:51:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 29 Feb 2024 23:51:01 GMT
USER ContainerUser
# Thu, 29 Feb 2024 23:51:01 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 23:51:11 GMT
COPY dir:b1b5f8b22673d55e5216fa8523c61ae3a55b9d2e6b8b7c225a467a0c2d76091e in C:\openjdk-23 
# Thu, 29 Feb 2024 23:51:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 29 Feb 2024 23:51:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9361c5977fbaed3b2410e6873784471f9176d02002008995f50459f646e93fe`  
		Last Modified: Thu, 29 Feb 2024 23:51:22 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281f85a3567eedba4f6a2eb5a715bf999a313a1f78d084f36b0ef2a5a8ca9022`  
		Last Modified: Thu, 29 Feb 2024 23:51:22 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0463f3d7420a95104040d4395f4bcf484e4ce4e051cf7bd564f38516030c7c67`  
		Last Modified: Thu, 29 Feb 2024 23:51:21 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadd3a50fee8f254129cca5f7e7d049ac368117f3a340904f9aad1f0c2ea67d9`  
		Last Modified: Thu, 29 Feb 2024 23:51:21 GMT  
		Size: 67.5 KB (67509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74af03fd2078363b316784e3e427a9deb0729f2c72dcfbd0e1ffc6623f3521f`  
		Last Modified: Thu, 29 Feb 2024 23:51:20 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a593c1df129da7ff4a07a119e76e1c81664800fac6de6d83074bd271ee0405ad`  
		Last Modified: Thu, 29 Feb 2024 23:51:20 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817128c7904d7d358d282aca1eedac889999db449f3e6fa0b9da385aa25ee522`  
		Last Modified: Thu, 29 Feb 2024 23:51:30 GMT  
		Size: 197.5 MB (197541629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf57978ba6dc1df2c5fbc901bb0d4f07ae1002787cdddb71b6942d7a9941497`  
		Last Modified: Thu, 29 Feb 2024 23:51:20 GMT  
		Size: 3.8 MB (3833979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bf7cfc6f1570d2277aba607da74075339fc4ec11e1a0d4a02b5ad269fd4b32`  
		Last Modified: Thu, 29 Feb 2024 23:51:20 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
