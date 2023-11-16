## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:07018ac998fd8b7188539d50d96b640302ed11054721f1e9e65de9a921e14bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull eclipse-temurin@sha256:1921186d834725209c3570a820a078b071aaa0b2229e3691eaa85a5339dde7f3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298624406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b7e57f0794560b567cfb92e7855917097c764221e691e632cbbdf51bcb024c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 01:41:12 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 01:51:25 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Thu, 16 Nov 2023 01:51:26 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 16 Nov 2023 01:51:26 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 01:51:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 01:51:38 GMT
USER ContainerUser
# Thu, 16 Nov 2023 01:51:54 GMT
COPY dir:3378004dd1c559f9d7d6f4bacd149386aa6ab741f7dba391fbd8a10b1a80b205 in C:\openjdk-11 
# Thu, 16 Nov 2023 01:52:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Nov 2023 01:52:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5c133738aab79d4c21c47e77cb838e2d00166f5e3e2632177622f67488259`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4310155f8eee56b296d809c0b64c304b9eb3a29e2f1d02624f32c177cea95882`  
		Last Modified: Thu, 16 Nov 2023 02:30:49 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650e34bd545b29edcc2ae1affdae2a78a27f414d2209a19da4dbc369bdcbb686`  
		Last Modified: Thu, 16 Nov 2023 02:30:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99cc8499cc732cad3ae9183c5dbbbfd8108c86124844783a2b2593c0e3e8f6d`  
		Last Modified: Thu, 16 Nov 2023 02:30:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97ecbccad5d7f6feacf54e359e81a90cb90b80773cd9000e04b3ecbc011b51b`  
		Last Modified: Thu, 16 Nov 2023 02:30:45 GMT  
		Size: 68.7 KB (68689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af0fcd14761493fc6db7fc3e0ee0a2aa3f69e8c62004c86ffb367b875a276d2`  
		Last Modified: Thu, 16 Nov 2023 02:30:45 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de83016c33857b55fb7388b994f7294e76ef6b716b09f4bc526a1d87d453d14`  
		Last Modified: Thu, 16 Nov 2023 02:31:04 GMT  
		Size: 194.0 MB (193969933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31a6befc69cd78ebbd218fe16cb01b1ae73aba0d6be241244ca34c9d3e1108`  
		Last Modified: Thu, 16 Nov 2023 02:30:45 GMT  
		Size: 81.5 KB (81469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aa411a77fa77c69cb5db7e8d49341958fcc94d097b60449718832f70518cfb`  
		Last Modified: Thu, 16 Nov 2023 02:30:45 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
