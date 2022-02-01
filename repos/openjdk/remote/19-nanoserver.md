## `openjdk:19-nanoserver`

```console
$ docker pull openjdk@sha256:af7d6ab58d77cd196096faf433646f2094664fa9746a9bd9bfe1fd662ab60519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:19-nanoserver` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:48f6768a93f2cdd8aee80a334d0e27707675cde1ad8a021253270f3fc2ef599f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 MB (291561697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8d7eacba4bf0a741753f87e98eaf058be547e65a727fae74044af658e8e211`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 19 Jan 2022 22:25:45 GMT
SHELL [cmd /s /c]
# Wed, 19 Jan 2022 22:25:45 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 19 Jan 2022 22:25:46 GMT
USER ContainerAdministrator
# Wed, 19 Jan 2022 22:25:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 19 Jan 2022 22:26:00 GMT
USER ContainerUser
# Tue, 01 Feb 2022 03:25:25 GMT
ENV JAVA_VERSION=19-ea+7
# Tue, 01 Feb 2022 03:25:56 GMT
COPY dir:83e6dc8bfef2dd7ea20c24b505ec03be5ab56f885aa3d9848383178e16d58634 in C:\openjdk-19 
# Tue, 01 Feb 2022 03:26:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 01 Feb 2022 03:26:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a1b3e13bb7b3d4b61b5f49a91d6eb9bfcf5539ab89c3687d608f17713c2409b5`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37e2d9d248af5cc77da02f6689e73057a6b209b1e2cc18d237e2225251d508c`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a757e837e961d995033dd26e4129e5adf88e7675118d83eb95cfccdd2f5170`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8711fe31967a4951c1345f1b126afe50ed968967c304e43d8e05224db1186e7f`  
		Last Modified: Thu, 20 Jan 2022 02:21:29 GMT  
		Size: 72.5 KB (72539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0481682eb573fcc3023c5291f96696ee373749cac12ceec16c1f2a990b142e78`  
		Last Modified: Thu, 20 Jan 2022 02:21:27 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9224bb5c93109af7faa5faaec568ace7c100077a3cdb81e93df350203fd4df`  
		Last Modified: Tue, 01 Feb 2022 03:41:45 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f674e1c3cafb3e99cc52237ba6eac06980299a93d716c5b6834a0933df2b8bf`  
		Last Modified: Tue, 01 Feb 2022 03:42:08 GMT  
		Size: 184.9 MB (184917859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f67bdfc55b2bed376149622a3a2b5054bcc91c9d5b2ec54f5e4682abbdfbe65`  
		Last Modified: Tue, 01 Feb 2022 03:41:47 GMT  
		Size: 3.5 MB (3517830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddce6804cbe57b732a1feffd8f65d677b968e07ec490367cc196c52e506c867`  
		Last Modified: Tue, 01 Feb 2022 03:41:46 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
