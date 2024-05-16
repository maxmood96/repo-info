## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:3b41870b72e32decabfea3ff88a093603bc3bc7f59e2254bbba0cc733b8cf159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:b7778ead9128bf78ea94d47ee8d56eb7e093512f4083eea853a8093e88ea21dd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198452765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5796a4d6d263c534adf06760c8101969c519727d7e28f02a72a7e296f2eb23da`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 15 May 2024 19:58:44 GMT
COPY dir:b092036da9619d86aad01e40fe92454a038bf12563d3a63208d5f3f51004688a in C:\openjdk-11 
# Wed, 15 May 2024 19:58:57 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:cac2e3c280efa8e53c5bd1ba0016654255efe3e906ce8049e43a9c135d6316ea`  
		Last Modified: Wed, 15 May 2024 20:49:47 GMT  
		Size: 43.4 MB (43384584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c24748585382891482466977e06a19ad2c4d1420d5af2bb828afc1e4be957ec`  
		Last Modified: Wed, 15 May 2024 20:49:39 GMT  
		Size: 49.5 KB (49549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
