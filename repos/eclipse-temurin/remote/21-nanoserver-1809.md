## `eclipse-temurin:21-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ed391943e24e6cf35983f26229b9c4f5de157f1e7e792862670c01d56fef04cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:21-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:dcf71dc3687eba8c3f8290c4ab1d0d4f5aa2b15abbeae065cb019e9569d0fd06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312292302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d039b03e62835a0519a23bc9f7a73b48a2f77ee47f32a531b853e165988ab9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 02:52:45 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:52:48 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 09 Apr 2025 02:52:48 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Apr 2025 02:52:49 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:52:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 02:52:53 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:53:01 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Wed, 09 Apr 2025 02:53:06 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 02:53:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5ec35a1c747082270344b596202219a29b47f141bfcb21d531fd2378a85f61`  
		Last Modified: Wed, 09 Apr 2025 02:53:11 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744cf1c63b5abda24a95e14e810f08a2d8fc02f478c8568a4ef62147960b52fe`  
		Last Modified: Wed, 09 Apr 2025 02:53:10 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d529dd9e1cb63a1c8da2a70d1fcb93068d939f7fc3e0b429a533f29c63e71a18`  
		Last Modified: Wed, 09 Apr 2025 02:53:10 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b5c7788df208df865f65883b163b7d51dc00c180dc3ffc8d027d37e7f6c035`  
		Last Modified: Wed, 09 Apr 2025 02:53:10 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ff3c1e42d8fd03da301dc07bd32006fa40dddd9c5672b583f5718f2f0cfc48`  
		Last Modified: Wed, 09 Apr 2025 02:53:09 GMT  
		Size: 70.7 KB (70706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eb7bab803758e6f0d4ccc8a3628174fb2751cac45c83732e9c467a375d2639`  
		Last Modified: Wed, 09 Apr 2025 02:53:09 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c8a3e7c4bb4bf14cd0f1c7e88ef9d8afe4ce07f4f39c28a8e08867aaf6bbda`  
		Last Modified: Wed, 09 Apr 2025 02:53:21 GMT  
		Size: 201.5 MB (201475550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ebbc5dd456f1ade84e0becf975fc22483119a9697cf89672f62c3e4447951b`  
		Last Modified: Wed, 09 Apr 2025 02:53:10 GMT  
		Size: 3.8 MB (3817283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227e8c3aecad0841df03fd7604fdff484eaebdc3e0cdc3b1188b2cb7e284bf02`  
		Last Modified: Wed, 09 Apr 2025 02:53:09 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
