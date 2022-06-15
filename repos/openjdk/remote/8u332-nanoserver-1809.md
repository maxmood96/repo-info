## `openjdk:8u332-nanoserver-1809`

```console
$ docker pull openjdk@sha256:fe91af0e8e76a10a8eff1ae6652085d30484a73516960531af13b9bb9e693c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `openjdk:8u332-nanoserver-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull openjdk@sha256:78673af0255595bb14b4e65106bbe2ea0815d21e5c3ae370af84a0097549ca17
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204280557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3b1e266177bb4e57a3ba0c1770ef3b4d87e1acdf70fca90c51c640c4a6857a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 17:30:58 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 19:55:29 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jun 2022 19:55:30 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 19:55:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 Jun 2022 19:55:40 GMT
USER ContainerUser
# Wed, 15 Jun 2022 19:55:41 GMT
ENV JAVA_VERSION=8u332
# Wed, 15 Jun 2022 19:55:57 GMT
COPY dir:679ecdc3b1aa3045788b8b611f7a86f57009d803f478419678a6098b0a258b48 in C:\openjdk-8 
# Wed, 15 Jun 2022 19:56:21 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92b4c385cd5cbb12fb09cb31c12b5e5de38cf7b380c8681286caac242c06d3ed`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cd545b01222a3eb04f8091b19b0f889a28bfdc13c5fb8f3ca93d64a4f12104`  
		Last Modified: Wed, 15 Jun 2022 20:26:22 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1c9f969ce25e06b9af4b5535d4cdde9a61e95b91f1b45f23098b7d5e5bb386`  
		Last Modified: Wed, 15 Jun 2022 20:26:22 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0455853e8a7516ff71a0bea8cb1ba9e5714b59b6d457b79c3e573b7a97400b8d`  
		Last Modified: Wed, 15 Jun 2022 20:26:20 GMT  
		Size: 71.1 KB (71065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae1eb2b55617f949b8f06a2d7702328e41dbe0146194fd91ffb4ff676605547`  
		Last Modified: Wed, 15 Jun 2022 20:26:19 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3408c8159fcf4f878f0051f5f0c31117e509e5b7d13a1d1a27ae06b68a139a`  
		Last Modified: Wed, 15 Jun 2022 20:26:20 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccced726847bc895eaeda4d2af607d23ae673aab1d844580ac03c07e49557bef`  
		Last Modified: Wed, 15 Jun 2022 20:26:33 GMT  
		Size: 101.0 MB (100950697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0af8bee691a4941b618062c94ea7bfa46454d8b49d65ee0f6b5a5f81ab6a29`  
		Last Modified: Wed, 15 Jun 2022 20:26:20 GMT  
		Size: 99.7 KB (99709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
