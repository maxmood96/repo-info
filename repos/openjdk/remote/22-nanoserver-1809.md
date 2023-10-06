## `openjdk:22-nanoserver-1809`

```console
$ docker pull openjdk@sha256:b9bf1e10ce81faa6f9f6f1f51838cfa9ef28466babc144c3d2d1760564d0cbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `openjdk:22-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull openjdk@sha256:224afcc48d47117fa6a4796279e4e92f343646633e23fad7ef8a07ac04382733
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307533530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8c6974b1ee2676232e8446ab6fc2c407259e387ea4406ad44a8c4fc0856add`
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
# Fri, 06 Oct 2023 19:25:40 GMT
ENV JAVA_VERSION=22-ea+18
# Fri, 06 Oct 2023 19:25:58 GMT
COPY dir:cdb676c7e47998ad35b8028b63314ad3ca3556dd433bebfc48557cc58d5a880e in C:\openjdk-22 
# Fri, 06 Oct 2023 19:26:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 06 Oct 2023 19:26:12 GMT
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
	-	`sha256:ee659c505bd4b6760171e6d681554bc011b8c0fbfa271c8a21ef0b83790848cc`  
		Last Modified: Fri, 06 Oct 2023 19:28:12 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8066474d46b3a044daf7af18d2841d0f2a25456054909c417f3976adb6cf347d`  
		Last Modified: Fri, 06 Oct 2023 19:28:31 GMT  
		Size: 199.1 MB (199140487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b88b1f2d0c247389215a81486be341e703a3c81cc1cba4f5e14d3d5f4bb34eb`  
		Last Modified: Fri, 06 Oct 2023 19:28:13 GMT  
		Size: 3.8 MB (3814054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a8215067b985bec1fea2c389ceef52e9c664254c91981e3514d1342073e3a3`  
		Last Modified: Fri, 06 Oct 2023 19:28:12 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
