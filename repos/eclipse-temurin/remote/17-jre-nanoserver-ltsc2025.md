## `eclipse-temurin:17-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:580778031d46c0fa9715badcf93ccf03319ed79331f21a064ae195b609bb97b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:2c38532b9f59857f23fe0c3e569f5fefd6fe69de3cecdececaad2474b963d980
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243687780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40487cee7fc7ee66212de4b005c5615976d907862144fb8acc8c37c360f05d9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:12:59 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:13:00 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 14 Apr 2026 22:13:01 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 14 Apr 2026 22:13:02 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:13:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:13:10 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:13:25 GMT
COPY dir:064fca0b30194d02fe341355ba6a62fc1748c82418561395eb5bec357779f4c8 in C:\openjdk-17 
# Tue, 14 Apr 2026 22:13:29 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fab16038e8768a85d71d774317652896fe519ce0557c309ae645abc360a1d30`  
		Last Modified: Tue, 14 Apr 2026 22:13:35 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03832eaf5412137cf1d98a1fe6878de7fa5d57efe340ad92048b0573ea245fb8`  
		Last Modified: Tue, 14 Apr 2026 22:13:34 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c06a28a22e88176227c7586673cd561f6fbb6c5baa853a378abf95d5ab34ba`  
		Last Modified: Tue, 14 Apr 2026 22:13:34 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d26e513aeebbab15ba967ddb1d6335ebe14621aff128bd2522088aaf093dc3`  
		Last Modified: Tue, 14 Apr 2026 22:13:33 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff69300c6d12696294f6ac206a6999bd519f2ea19204fab260b4e14b3436510`  
		Last Modified: Tue, 14 Apr 2026 22:13:33 GMT  
		Size: 75.2 KB (75217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8c694a03d7e7ed1b236e34812374573633a5b897347387a5a40a1a3557dd89`  
		Last Modified: Tue, 14 Apr 2026 22:13:33 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239b2ee27df9607dc609ca82ad7e5e45741e8d43768953ae28aaffc5a151aebf`  
		Last Modified: Tue, 14 Apr 2026 22:13:39 GMT  
		Size: 43.8 MB (43794842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55004935276e4cb651fe2a0a398ad79c994b71017685ec323a4e0b4f55ae34f`  
		Last Modified: Tue, 14 Apr 2026 22:13:33 GMT  
		Size: 95.3 KB (95332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
