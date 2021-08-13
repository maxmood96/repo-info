## `openjdk:18-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:6f82bf44a6e2117367b88993f159ecc5fae483eb6aa491bc7eb1fd3eac6cb90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `openjdk:18-ea-jdk-nanoserver` - windows version 10.0.17763.2114; amd64

```console
$ docker pull openjdk@sha256:9134db81c8f43ad43fc5c791fda398ca8776860c0f948f6d37a0f377dd184700
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289020226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea960422fcf5ed1f27d2c7b1f6d039fc3dc0bc0309b0538a8a5fbfb54cdf670`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Wed, 11 Aug 2021 17:30:38 GMT
SHELL [cmd /s /c]
# Wed, 11 Aug 2021 17:30:40 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 11 Aug 2021 17:30:43 GMT
USER ContainerAdministrator
# Wed, 11 Aug 2021 17:31:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Aug 2021 17:31:09 GMT
USER ContainerUser
# Fri, 13 Aug 2021 18:18:59 GMT
ENV JAVA_VERSION=18-ea+10
# Fri, 13 Aug 2021 18:19:19 GMT
COPY dir:1fdada6bd55ad5c1c569078f7bd19c2c0a4439bfe65981fd3a7baa8b95c56f6a in C:\openjdk-18 
# Fri, 13 Aug 2021 18:19:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 13 Aug 2021 18:19:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae0a5a946be2ad0e39a8260e454c0060a31a9f7e5be75d1f9038dc13730abc0a`  
		Last Modified: Wed, 11 Aug 2021 18:21:28 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3e3ce6f906341a31b594d25772e87453477f92df500f7e55c033ee65d1f7b8`  
		Last Modified: Wed, 11 Aug 2021 18:21:27 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4140a377a80813839c51929577daa32b3f49ead3975b3b71a2106af7999f7c`  
		Last Modified: Wed, 11 Aug 2021 18:21:28 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeec1a666d3ea4495353e16515d8a87648b15d6c51c137b53bfba178aa5a36b`  
		Last Modified: Wed, 11 Aug 2021 18:21:27 GMT  
		Size: 68.6 KB (68571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bce606c6fc4ebc45e038cdeefb933ddc75feed60a9793ef5682fcacbeb615c`  
		Last Modified: Wed, 11 Aug 2021 18:21:24 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2383b5c38046bd7dec2b9004a10c94fa0053af3e2c061f5e3100273a10aefc9`  
		Last Modified: Fri, 13 Aug 2021 18:25:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47281a936627da3a9f0a9640b2e968f1c84f709e04f31c65fefc23e41edca77d`  
		Last Modified: Fri, 13 Aug 2021 18:25:38 GMT  
		Size: 182.6 MB (182589540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1212cb99efdd763b8411dfbbf8bb9b4f14cb0f0f17ae74a8b3272875cd66d7df`  
		Last Modified: Fri, 13 Aug 2021 18:25:22 GMT  
		Size: 3.6 MB (3613945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f974f8295c1f0452b9fefaea9af12b6e2d3540c741b5790b807a31cba63923a`  
		Last Modified: Fri, 13 Aug 2021 18:25:19 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
