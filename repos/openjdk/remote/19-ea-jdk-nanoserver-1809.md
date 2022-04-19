## `openjdk:19-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:155313ea1ca4874ee2970efe1e5fca45a31269544ae48d90bcba95716c43b909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `openjdk:19-ea-jdk-nanoserver-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull openjdk@sha256:9765ed080486f2001b61ef3107a902bda83858cb5ba5664ef63afe2a08fa4396
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296407076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899afea45a099da1e5229e2f594e958885175ff673070eb377b2f2957c331d23`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 15:16:11 GMT
SHELL [cmd /s /c]
# Wed, 13 Apr 2022 17:00:37 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 13 Apr 2022 17:00:38 GMT
USER ContainerAdministrator
# Wed, 13 Apr 2022 17:00:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Apr 2022 17:00:44 GMT
USER ContainerUser
# Tue, 19 Apr 2022 00:44:05 GMT
ENV JAVA_VERSION=19-ea+18
# Tue, 19 Apr 2022 00:44:18 GMT
COPY dir:c4937bbfb739827c039ab01e9d7f4d0872e04cc2c36687d81aba82da6051f9a2 in C:\openjdk-19 
# Tue, 19 Apr 2022 00:44:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 19 Apr 2022 00:44:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ea4009814dceb50337c66614a6008cfc2fb73ce53e62162bce071ef6ea1adf2d`  
		Last Modified: Wed, 13 Apr 2022 15:58:06 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4644baf69a04abfb80da969c1fb009552c461553f3672bd4e787c0ac7c37ea`  
		Last Modified: Tue, 19 Apr 2022 00:53:51 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61095df7d33e436b0d9cb0052f433e155a897f4278b9dc0a8d13582d6cad38ad`  
		Last Modified: Tue, 19 Apr 2022 00:53:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2110ca10faf88314f61157ce6bfeb157b8b8eebd74be6f0a78f2f7b82c514a`  
		Last Modified: Tue, 19 Apr 2022 00:53:51 GMT  
		Size: 68.8 KB (68813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd03d4716f16fd9ebec77b5cf5099ed25d889884b5a06da589ce896a7db47a15`  
		Last Modified: Tue, 19 Apr 2022 00:53:49 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6c9b244c1a963011fb273b13e9230b1155ca39a80390f7b73f2e547b37ea00`  
		Last Modified: Tue, 19 Apr 2022 00:53:49 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d600e4b590f6a26b8767e3ccd3ad53a278d6e914e7d3295ed7dc81a443174ad`  
		Last Modified: Tue, 19 Apr 2022 00:54:09 GMT  
		Size: 189.6 MB (189624544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c653974d9f694711086fac12babb4425fcdd62a6bbf1eccee4107ba9587c9ba6`  
		Last Modified: Tue, 19 Apr 2022 00:53:50 GMT  
		Size: 3.6 MB (3610766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bbab391d9abe871dde4c3e9ec6f3428e3877d5540a3f9fe0d633b10c1d4c2a`  
		Last Modified: Tue, 19 Apr 2022 00:53:49 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
