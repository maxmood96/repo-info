## `eclipse-temurin:8u442-b06-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:9bfbc8389ad3b08ab1fd6f9e255d080ae773b4dcd95d4cf904c1a86526217e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:8u442-b06-jre-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:f733bd0b1682be3e5ca869346d32aff9c6378e2328601d2a37ffa07ad6678773
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195961533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465013bb7397ee88055117734d7d2077759204e7979f712e6fc9082206e9061b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 02:11:09 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:10 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 02:11:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 31 Jan 2025 02:11:13 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:11:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:11:20 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:11:23 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Fri, 31 Jan 2025 02:11:26 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0cc82873365f2feabbb386b072fb8175769ab45797a02f74e35c58599e3da5`  
		Last Modified: Fri, 31 Jan 2025 02:11:32 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381fa43710e9b81837a823850a4f28cc1741bae8272819b386dd12d849876eaa`  
		Last Modified: Fri, 31 Jan 2025 02:11:32 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086ffd69b6a04457b467cb16e44461157ca2aa3db1c72207925e0c64fd529680`  
		Last Modified: Fri, 31 Jan 2025 02:11:32 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e47ea8fc74b803fed9050e49e65e653897d77ec6bb52a470b080f3dff6f36f`  
		Last Modified: Fri, 31 Jan 2025 02:11:30 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2a41a22817a98152a21312012cdba5dcde76626d98372ff5c84872c738a240`  
		Last Modified: Fri, 31 Jan 2025 02:11:30 GMT  
		Size: 68.6 KB (68605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b60705ff134a52697d46aeab5cfda4b5a36d5d403b0a6e6c6131b7f79c219e3`  
		Last Modified: Fri, 31 Jan 2025 02:11:30 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7b0c7ee76e9b7f306cd4d02f62c949554ec166655c90f6c826038a8e9e2368`  
		Last Modified: Fri, 31 Jan 2025 02:11:34 GMT  
		Size: 40.6 MB (40552229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77db9ef61f989864f4962dae4334eaccc8fbc25bcce4af1cdb5d64435bf89774`  
		Last Modified: Fri, 31 Jan 2025 02:11:30 GMT  
		Size: 68.0 KB (67965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
