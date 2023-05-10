## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e98e1bad86f581a21172ed54eeb6e8e1288eac0f2295d3aaebd5f4eb6d57404f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull eclipse-temurin@sha256:72eaa5eb99a1d0ccfda1f01da57c64b61d715987a310a7ff0875b95b45e2c2dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297540103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f4c626c855d95a1d766b08730892ca831ef3c6160776147e0a9a939fb5c4f9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 00:40:01 GMT
SHELL [cmd /s /c]
# Wed, 10 May 2023 00:49:34 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Wed, 10 May 2023 00:49:35 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 May 2023 00:49:35 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 00:49:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 May 2023 00:49:47 GMT
USER ContainerUser
# Wed, 10 May 2023 00:50:01 GMT
COPY dir:aa85dc89894032bdcf98e5da06633e8de4813537c791ddbe3fc8bdfa8596f8de in C:\openjdk-11 
# Wed, 10 May 2023 00:50:14 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 May 2023 00:50:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b79dd15c5dd82bc10521b9a4e49241f70088bc6edbb286f90be198abea55e23`  
		Last Modified: Wed, 10 May 2023 03:01:27 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55743eb2ae5cd042a272d7ca09db1dc320b97fffa4ff7a6f1f54dafa7878cf5b`  
		Last Modified: Wed, 10 May 2023 06:57:35 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be1c1d26b6510cb6c21b9f715964b78399dc78f00da502aac8e47eac3409d8b`  
		Last Modified: Wed, 10 May 2023 06:57:35 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8319d0c3865d1d122169d35a992638c1cdc3d03bd6576cfeda1ea349058398`  
		Last Modified: Wed, 10 May 2023 06:57:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5313d0be67fb1f48560d21400fa1b69a28bc27ebce45869109c6c43957cea9`  
		Last Modified: Wed, 10 May 2023 06:57:33 GMT  
		Size: 69.2 KB (69204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0189caad3d791abf9f86943871c0eab7b33b58471fd9931654ddffc928f8fbf`  
		Last Modified: Wed, 10 May 2023 06:57:33 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68af9329107780527490e505bdf82064c058f83d293edda2e8c73ca6fa9873bb`  
		Last Modified: Wed, 10 May 2023 06:57:50 GMT  
		Size: 193.0 MB (192983983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da07ae1bc4166e6374182781b0f17ed7d89dd604676282c7d819cd779527d30a`  
		Last Modified: Wed, 10 May 2023 06:57:33 GMT  
		Size: 96.1 KB (96085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca253b8c4bd5589a5959cfe78644b77ffd31f8753511bb3661880022fad7ab9`  
		Last Modified: Wed, 10 May 2023 06:57:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
