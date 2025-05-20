## `openjdk:25-nanoserver-1809`

```console
$ docker pull openjdk@sha256:13bf221fc80315effeb3f9527563b27a34789c3e804ba980742edd6ae53d7358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `openjdk:25-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull openjdk@sha256:bdcd5c81b51b25a86de94e953a21d7a1a4ab09b3ac257d1e6e260a7eb8acafec
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322213408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56dc9c074f346f456b4b26d3cd2a34f2c6be9b81e2be4fac14cb5ba96106cfa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Fri, 16 May 2025 21:13:04 GMT
SHELL [cmd /s /c]
# Fri, 16 May 2025 21:13:05 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 16 May 2025 21:13:05 GMT
USER ContainerAdministrator
# Fri, 16 May 2025 21:13:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 16 May 2025 21:13:08 GMT
USER ContainerUser
# Fri, 16 May 2025 21:13:09 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 21:13:18 GMT
COPY dir:be99341787be1c3f0d565e6ac1d9202629ef201376adf519d795dfb5baaa83fe in C:\openjdk-25 
# Fri, 16 May 2025 21:13:23 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 16 May 2025 21:13:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4019e06e6567532f9b346c4b6ac1ccedc26658952d08a8ce9fd192575fd30e`  
		Last Modified: Fri, 16 May 2025 21:13:28 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc585c8df9d64b97b1ffac6fa24bc283284bfbc270faa6c1b464fa1fa0432f7d`  
		Last Modified: Fri, 16 May 2025 21:13:27 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915f2422588ead042be2f223cc1b4acb177be94365a6254dd2a77f797e671652`  
		Last Modified: Fri, 16 May 2025 21:13:27 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eec5d40298775cf57d9af6a5bcb1180fb3f6de4ff7539c47ada2350aed707b8`  
		Last Modified: Fri, 16 May 2025 21:13:27 GMT  
		Size: 72.4 KB (72400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ca80c9ba0fbd14cedd8ce361250403d297674ae9efd2a8aacaedc5cbfee99b`  
		Last Modified: Fri, 16 May 2025 21:13:26 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292def4a5087f2c5e8b405466a20bf2bddc6d5f8b9f34b43ec23971609a1dfbb`  
		Last Modified: Fri, 16 May 2025 21:13:26 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28838afc16c74cf596587946d8fdcd6f6561692626b2fec3316fdd0e6d4ddb1c`  
		Last Modified: Fri, 16 May 2025 21:13:39 GMT  
		Size: 208.9 MB (208920575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3873193e3ac25d860de84c7854bb3ef91e6ffd338e18ed8c6ad849625ffb8440`  
		Last Modified: Fri, 16 May 2025 21:13:27 GMT  
		Size: 4.4 MB (4433214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dea3b3d5b0ae637dcb83466778eb4948781985f1ca4367ea8452a9237805c`  
		Last Modified: Fri, 16 May 2025 21:13:26 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
