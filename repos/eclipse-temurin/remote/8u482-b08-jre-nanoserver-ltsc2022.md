## `eclipse-temurin:8u482-b08-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:024e87eed9494f5c373bb49d2c7dec97b714ecee9ca94208987daaa3ac14cf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:8u482-b08-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:4a2c6a1efad9afc8136c87f9380aa1c8327a24b192a4ffd6430300fe9066e293
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167108580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8a8b10d7455f4035a3c2138cd7e8826121e3c59018732f69b55bf7645afb3f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:10:49 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:10:49 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 14 Apr 2026 22:10:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Apr 2026 22:10:50 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:10:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:10:52 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:10:55 GMT
COPY dir:e192ec1627bb02acae941746a6647cea6857b84f7daa4f746913822a0bac9dcc in C:\openjdk-8 
# Tue, 14 Apr 2026 22:10:58 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f577f04bf25fbe8b679de7ed1a1bb3aec05c54b5f22de311414b5b7e7dbe8fb5`  
		Last Modified: Tue, 14 Apr 2026 22:11:03 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627115c5acf0bbe2330d834f939b20ec42ae5eccd56fe9cdc017539a89542ace`  
		Last Modified: Tue, 14 Apr 2026 22:11:03 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3840c2e36b7730ef3c32fe05845e820a3d16d81acf6cb3c6d8eb64c4e10a88f4`  
		Last Modified: Tue, 14 Apr 2026 22:11:03 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2715f7d177c97b6cb40ef5e323b3c5b65fe73120058fc834a067470896507b8f`  
		Last Modified: Tue, 14 Apr 2026 22:11:02 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d645f38d3a895b39f6a169b107fe4293e94cd4b03e37d1475b8c8d7909dbabc`  
		Last Modified: Tue, 14 Apr 2026 22:11:02 GMT  
		Size: 76.7 KB (76726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5528f1e81988ed88686c4b1383a4eace5ee00eca1b1b30f2dfffc3d700711381`  
		Last Modified: Tue, 14 Apr 2026 22:11:02 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856de40e90ad12b653314e3c03cdef514e268b3a4140ba50e8f7c329bf5502e6`  
		Last Modified: Tue, 14 Apr 2026 22:11:06 GMT  
		Size: 40.0 MB (39969915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3a9e1809fc6cd00f664b50fc8b7ccf54c66c7290510c6051a79acfd153c60c`  
		Last Modified: Tue, 14 Apr 2026 22:11:02 GMT  
		Size: 100.7 KB (100692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
