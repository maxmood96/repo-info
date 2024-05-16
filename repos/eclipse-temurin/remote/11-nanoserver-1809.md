## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:de49cb733196b9c84a1635ce1cac2f1d6356f4083d9cd418dbfc6148371b5f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:a890bf4ea9bcaab6302129b66c1e16b8cc1de14c0e00f42d04c7411130434a7c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349163454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6b3ab3ab195d255216b2c38e1c538fccbd246de79159a24664f327ad04b877`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 19:42:01 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 19:53:09 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 15 May 2024 19:53:10 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 May 2024 19:53:10 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 19:53:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 19:53:20 GMT
USER ContainerUser
# Wed, 15 May 2024 19:53:36 GMT
COPY dir:8aa740e08efd9dadfa2fb1fd54d653720c8e2097106a2d2f0f8f1f0b127bcc3e in C:\openjdk-11 
# Wed, 15 May 2024 19:53:49 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 May 2024 19:53:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6a511fea8e874efc08e5058ac5b12b6433c36ba6570862a619dd80cfb0e190`  
		Last Modified: Wed, 15 May 2024 20:45:52 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c32e10802b36678aa44d14344ee9a4b6f31422a72479a968a8343d7097b624`  
		Last Modified: Wed, 15 May 2024 20:48:36 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081fc4ba1cda4e8eab199bb8c999c9fb97391b0b67f6f2812b0d0dfb789c05fc`  
		Last Modified: Wed, 15 May 2024 20:48:36 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d727411c1480386ca50ce84f705938185da575857a076a02a2f09ee34f9021f`  
		Last Modified: Wed, 15 May 2024 20:48:36 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdf64b6eeb4c8fcca65b62536a2a200a5ccdf8948211ab8c92a564646438de3`  
		Last Modified: Wed, 15 May 2024 20:48:34 GMT  
		Size: 71.5 KB (71532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b4ae3043cd60f0d4eadcbee4b2de8fe6f017d1d448329c07f4fb9b230a08ef`  
		Last Modified: Wed, 15 May 2024 20:48:34 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e24cc0b655aa09a6432db04ab070c06b97eccc8b8f3d7d56b2863446b233ca9`  
		Last Modified: Wed, 15 May 2024 20:48:52 GMT  
		Size: 194.1 MB (194084585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be946058a57c9c4319389291151efc70bed14e54d3f5a95c89e1c3115f5cabb`  
		Last Modified: Wed, 15 May 2024 20:48:34 GMT  
		Size: 59.1 KB (59067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2bcb5c1f70433eaa9fc8daf1c7b7f55a890a99787998c91171f501937bdc50`  
		Last Modified: Wed, 15 May 2024 20:48:34 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
