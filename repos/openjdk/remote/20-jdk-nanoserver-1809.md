## `openjdk:20-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:cda8f0902d9d22262fdd29245ac32ad24725030a09ed37ca6de7a48e14e0b69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `openjdk:20-jdk-nanoserver-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull openjdk@sha256:bd97a0d76fcbe2a9b6739505964140275b35b77e3680d2a9cc332f1c9778fc38
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298774271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e04d979aa5d1e3b8754bafec39c1426282f8a1740df7e4b1c9824ae316a665`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 17:30:58 GMT
SHELL [cmd /s /c]
# Thu, 16 Jun 2022 01:19:36 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 16 Jun 2022 01:19:37 GMT
USER ContainerAdministrator
# Thu, 16 Jun 2022 01:19:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Jun 2022 01:19:50 GMT
USER ContainerUser
# Tue, 12 Jul 2022 01:18:46 GMT
ENV JAVA_VERSION=20-ea+5
# Tue, 12 Jul 2022 01:19:01 GMT
COPY dir:ea52c40ffc8b78540b2df87805973951e9050aa754e630d8a0f152de6836b86d in C:\openjdk-20 
# Tue, 12 Jul 2022 01:19:27 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 12 Jul 2022 01:19:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92b4c385cd5cbb12fb09cb31c12b5e5de38cf7b380c8681286caac242c06d3ed`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda95a4aa1ce8b324ff84e1ccdf8befbe50e58a948d31b65618925e2842efada`  
		Last Modified: Thu, 16 Jun 2022 01:33:30 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f66084dce2c5c1fa8b13cd8edb172b48a4411ebf5466035c9c5fef517796cce`  
		Last Modified: Thu, 16 Jun 2022 01:33:30 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a225993ae008c14a2ad71f55edbcafc99d581fba5b2fd8297a2af9bd6fc2d`  
		Last Modified: Thu, 16 Jun 2022 01:33:30 GMT  
		Size: 71.2 KB (71215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1582199825c588de3fcfbec196a74a70813b8a78abaa2abbed131795de8f1d6`  
		Last Modified: Thu, 16 Jun 2022 01:33:27 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9425edcf54914d8501f5a3bab004c4a631ce79b84ace7458c3b2b1a12d2d765`  
		Last Modified: Tue, 12 Jul 2022 03:21:45 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bc61c5938bc2521d8a6570fe4a140feb42a8b5bf450d601b9fca24d51e2de3`  
		Last Modified: Tue, 12 Jul 2022 03:22:06 GMT  
		Size: 191.8 MB (191806416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f63a795ada72702614acaa8481e889803138fda0c9f186ec4a708c0a5d95686`  
		Last Modified: Tue, 12 Jul 2022 03:21:47 GMT  
		Size: 3.7 MB (3736423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680e3806d858bb91833a4a197c6f3bff0331b3bb245d735151ec281d43ce923f`  
		Last Modified: Tue, 12 Jul 2022 03:21:46 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
