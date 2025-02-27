## `openjdk:24-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:e6cbc0da42c4d42d7a9dd95f68eb8d82fc14484a08c5f945cfc48c8b97ce9f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `openjdk:24-nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull openjdk@sha256:acd4cbbf0130e51eb7ffaa9688de0c96a574f625dfd18715e221de74d49c6ac8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.6 MB (414592651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6b4b543f3d3963688623b3c8fbff171d21695336b8b7bef19f42c4457253bb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:13:47 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:13:47 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 27 Feb 2025 19:13:48 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:13:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 27 Feb 2025 19:13:51 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:13:51 GMT
ENV JAVA_VERSION=24
# Thu, 27 Feb 2025 19:13:58 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Thu, 27 Feb 2025 19:14:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 27 Feb 2025 19:14:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9092cd1188531750c102da49846819f50a4ffa4e998cf04b2cc5359e0b46393c`  
		Last Modified: Thu, 27 Feb 2025 19:14:11 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da81558aa0912f78379267b1485bc45f924e197cf35b6ea36a968446472cbb59`  
		Last Modified: Thu, 27 Feb 2025 19:14:10 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50d83ccb227b31a610316b6fdf8d25ab2827cc3d84540493a360c3a145eebcb`  
		Last Modified: Thu, 27 Feb 2025 19:14:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7d57bc4c8fd68572fe5da998b7b145d42ccd121ea8ed57c2e7fc7f10f8e537`  
		Last Modified: Thu, 27 Feb 2025 19:14:11 GMT  
		Size: 76.1 KB (76089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3daf0b4cdc70b169e92cd8576865a124da6f2d49306ea9ccfb47d3ef73d167d8`  
		Last Modified: Thu, 27 Feb 2025 19:14:09 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b44ab63de4aa56f77509748fd3cbb2842e8f7eeeeaa933d53a63953d2a8d5a`  
		Last Modified: Thu, 27 Feb 2025 19:14:09 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ed45f9edf540adc8bdec2f8001d3b8ba42d92a4d0fa5af0339964502f367ed`  
		Last Modified: Thu, 27 Feb 2025 19:14:20 GMT  
		Size: 208.5 MB (208526176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f903f313e3f2c20ed82a4b2d73bf3ed02033028ecc7e4e03f5dfd273f34403`  
		Last Modified: Thu, 27 Feb 2025 19:14:09 GMT  
		Size: 93.8 KB (93812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b321fe94742953cc5f0bebd3d721cf0072b2e61f8645876e2e2074d55c4bfff`  
		Last Modified: Thu, 27 Feb 2025 19:14:09 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
