## `openjdk:23-rc-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:c85b3e2e913fbac87fc620cef03d8866514694a49425e8ebb6f8f3d6c40cd2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:23-rc-jdk-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:7b1816f6bedd5042ef716d2d3276d01fca2fc0f62a1e871375acf6d13235eb47
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365341083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ccd3ae391a054620756602cb6dd63a3ce8352442e21eab90fae828c166eb97`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 21:12:42 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 21:12:42 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 13 Aug 2024 21:12:43 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 21:12:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 13 Aug 2024 21:12:46 GMT
USER ContainerUser
# Tue, 13 Aug 2024 21:12:46 GMT
ENV JAVA_VERSION=23
# Tue, 13 Aug 2024 21:12:53 GMT
COPY dir:7f285cee4711ed5c5f7c87b2783489a3640a2db87c0fcb661fcbc1197c78fec4 in C:\openjdk-23 
# Tue, 13 Aug 2024 21:12:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 13 Aug 2024 21:12:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20b9733b98592a04e2dc2bbca05f1344617f62eb5063210ca4639da09554ffe`  
		Last Modified: Tue, 13 Aug 2024 21:13:05 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8609c7ad7e06f705c2468722ad7cf99499d87a2c3c64d15e052946dcb71798`  
		Last Modified: Tue, 13 Aug 2024 21:13:05 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351d3fd151a20fafbe4d31e8f74f6b69374b7123857c0a5c8cc619d482d14cb3`  
		Last Modified: Tue, 13 Aug 2024 21:13:05 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0755b53e0d38cbf32602798c44be97f9a30dc97f014e275dbc17263b077ff760`  
		Last Modified: Tue, 13 Aug 2024 21:13:05 GMT  
		Size: 73.9 KB (73857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa254e307501580796d75810373fc168db35d12b70cefb087734477cb272161`  
		Last Modified: Tue, 13 Aug 2024 21:13:03 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae22203652f7d12441ddca57d407dc7d464e29bafb30c60c2c7629b9a84d18`  
		Last Modified: Tue, 13 Aug 2024 21:13:03 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf69733a4d9bcbcaaccac3c60dcb45005dd45e6016bae33c50ffe27167ba2873`  
		Last Modified: Tue, 13 Aug 2024 21:13:14 GMT  
		Size: 206.0 MB (206042264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc065b0bf3b6dfe7998db07fdea061cdae49f3624cb0776385bcc2a44b1dd81`  
		Last Modified: Tue, 13 Aug 2024 21:13:04 GMT  
		Size: 4.1 MB (4135483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481665e7ef449f30a10a8efc050eeaa60f2d0efa7620ce5cd20f92a014249d19`  
		Last Modified: Tue, 13 Aug 2024 21:13:03 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
