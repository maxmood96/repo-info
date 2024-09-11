## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:2e4c8b72be5db54f55cc2f9111d980a00875c618efbec03fda17763002109bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:47e03d38e48551669eb20ba6b5161f10f03c3bdee8016ab952a99555a84b1461
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345218614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2055c6caf99331404a2ed6a75298b48a9aeee8f616f41c950556243dfade22df`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:38:01 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 00:50:23 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 11 Sep 2024 00:50:24 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 11 Sep 2024 00:50:25 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 00:50:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 00:50:33 GMT
USER ContainerUser
# Wed, 11 Sep 2024 00:50:45 GMT
COPY dir:11f935f87b5561ba9de5a02e585d9b073f4114e9ab1765209f28e6005e01c91d in C:\openjdk-17 
# Wed, 11 Sep 2024 00:50:55 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Sep 2024 00:50:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340318059288cbbdb326eea5b7079e789361251409038a37867d4e395c9404a5`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91950d63fc5ef50eff89ea5d9b367978ab15d1e8be06ea71699f45ef2aa3fd09`  
		Last Modified: Wed, 11 Sep 2024 01:26:28 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f5a9c07212454d0e55d94a8bf0c20857e04ea2239ce45e54b6dc2e3427b2e6`  
		Last Modified: Wed, 11 Sep 2024 01:26:28 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec22c9c1b01867beec0be83f2b95feecea9d4d3f8eb581673baf3b5a462ae553`  
		Last Modified: Wed, 11 Sep 2024 01:26:28 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099df04b57eb6987eb23da28ae2dc75eb6f0e9237082b3d2c99cf620b7304c02`  
		Last Modified: Wed, 11 Sep 2024 01:26:27 GMT  
		Size: 67.5 KB (67532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a75f0f06fa9dfcf8547164899e5cf4c6ac8a7ac73e9a4a149b98dbb15febe9`  
		Last Modified: Wed, 11 Sep 2024 01:26:26 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee67e13e9c37ab4591424551d2bb61eca03d651475e51fc4ac931d0e1bc770c`  
		Last Modified: Wed, 11 Sep 2024 01:26:43 GMT  
		Size: 186.5 MB (186458874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83d732fce07c40d3308e23645af79fb2b34500f8292b326f3c062ae77f66a4b`  
		Last Modified: Wed, 11 Sep 2024 01:26:28 GMT  
		Size: 3.6 MB (3604486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6030141a06fa33a75e5416cfa3d43ce8b0504e07c42d09c701aab1f3c5939bd2`  
		Last Modified: Wed, 11 Sep 2024 01:26:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
