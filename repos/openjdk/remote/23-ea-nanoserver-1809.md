## `openjdk:23-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:6cfb2b6a3cf80ac899205fec5bb366223883b3ba31a404bc6bc2a8e07037b474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:23-ea-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:36a2a259f30687cf68eff99e69311094f0f4108d547c421586c36cd4bee8c0a9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306101527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6385eca7ce47b0b8d9e84a2c15a0e9870687ccdb03dc8dcd68ae4924f17ef3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:04:37 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 21:04:39 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 14 Feb 2024 21:04:41 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 21:04:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Feb 2024 21:04:44 GMT
USER ContainerUser
# Wed, 14 Feb 2024 21:04:45 GMT
ENV JAVA_VERSION=23-ea+8
# Wed, 14 Feb 2024 21:04:53 GMT
COPY dir:6a84c5cee471a7abf9cef5fcb4872f5f6ecc20119671264fac429d350b8b4ca7 in C:\openjdk-23 
# Wed, 14 Feb 2024 21:05:01 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Feb 2024 21:05:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cae8b08be6ef504d59c12b5d6fa74603ecfdd9f3b057a58838d02edb0af5240`  
		Last Modified: Wed, 14 Feb 2024 21:05:10 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a1fdaa8f2479af2938d24c62b47b012b9cca20c9ce258c153afd64d2c6b2ce`  
		Last Modified: Wed, 14 Feb 2024 21:05:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493177220a613276deb63ed07e9bb504a8ed1131cfb650b6f8ecfe0cc268c8b2`  
		Last Modified: Wed, 14 Feb 2024 21:05:09 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ccb252b0aeea190eb16622732111cf06b723cae19a8947e9132118cad5c273`  
		Last Modified: Wed, 14 Feb 2024 21:05:09 GMT  
		Size: 83.8 KB (83778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dd3f691d429b23ef616e7f5b613f146419b5f6994d025b8c4a8cd286b02321`  
		Last Modified: Wed, 14 Feb 2024 21:05:07 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abf50d238eac60f83856eee8f72077e4291d6e4d996cf663521dd713e0372d3`  
		Last Modified: Wed, 14 Feb 2024 21:05:07 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8ca80478f24bf927f405dbb6baf1cf865f552c54d4dbf9cec63a09ee66251a`  
		Last Modified: Wed, 14 Feb 2024 21:05:19 GMT  
		Size: 197.5 MB (197520338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e9dc52d44d4609ceea5639af83de6b2b603666457054cad999e593188ed240`  
		Last Modified: Wed, 14 Feb 2024 21:05:08 GMT  
		Size: 3.9 MB (3869586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00931e945a186c3889b92a5bd1ace041bfe6afdea4fac41a50c115707fe9e65b`  
		Last Modified: Wed, 14 Feb 2024 21:05:07 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
