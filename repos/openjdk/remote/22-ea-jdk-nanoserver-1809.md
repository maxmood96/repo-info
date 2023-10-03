## `openjdk:22-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:c4a24b992c85802f23e425605ef553c3bb7e3dd7c4ebb599f898fcf14cd7b7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `openjdk:22-ea-jdk-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull openjdk@sha256:ee3caf3870b19ac6d780341fc901e48e8b55af558b3e98e33dc521f719be10cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307519746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b385d72ad04d9e2ceccc0a3d69cf60daf2acdebe0b2c0bae5ab57ad1db619c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 02:29:44 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 05:19:19 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 13 Sep 2023 05:19:19 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 05:19:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Sep 2023 05:19:25 GMT
USER ContainerUser
# Tue, 03 Oct 2023 01:34:45 GMT
ENV JAVA_VERSION=22-ea+17
# Tue, 03 Oct 2023 01:35:01 GMT
COPY dir:c0ab04eeaa137872b3d0c9d14e7f5562878e27c079c271f631a011da2b0e3972 in C:\openjdk-22 
# Tue, 03 Oct 2023 01:35:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 03 Oct 2023 01:35:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5bcbc9b0f0398bf8f14c235b24ba85d9acacf855518119cd1ce338a235a15`  
		Last Modified: Wed, 13 Sep 2023 03:36:33 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6f344751fdeca77c774720f1f5845e2a683d1ed1b251bd6e554f91ab03d2b0`  
		Last Modified: Wed, 13 Sep 2023 05:26:46 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be8c52d7c546ce325f7f3606c55b22e94fd1925aba26440028f33d2a873ff1`  
		Last Modified: Wed, 13 Sep 2023 05:26:46 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de794e4f653951d19d788489e6c197cbbaa2864a36a169d068b25cf13ea0c6a6`  
		Last Modified: Wed, 13 Sep 2023 05:26:46 GMT  
		Size: 79.5 KB (79476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4673df9416ca713de65ecb18e35ecfcad8bafedd6b1e61dca148de841d138b7`  
		Last Modified: Wed, 13 Sep 2023 05:26:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7916caac33c1a6a7896d712dad1b2a5017f6acff87503c96ad8956784a63cef4`  
		Last Modified: Tue, 03 Oct 2023 01:37:17 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761e397282f480d03afd55fed40a7886a3e203d2b4d86147b9e4be941a799605`  
		Last Modified: Tue, 03 Oct 2023 01:37:38 GMT  
		Size: 199.1 MB (199127760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b954600a7b76705780f2664f14de5c62a14c526eb0e6370ebce2921ae47ce16`  
		Last Modified: Tue, 03 Oct 2023 01:37:18 GMT  
		Size: 3.8 MB (3813030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57813c1ea7430fb4e6f2be81844e366162b703d776fd4a171b26878d73acb28a`  
		Last Modified: Tue, 03 Oct 2023 01:37:17 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
