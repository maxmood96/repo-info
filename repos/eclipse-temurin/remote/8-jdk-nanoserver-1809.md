## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f0b3feba584c21ce3499228a9d6dddf4141300a6783cbf1c1d28a07832a173d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull eclipse-temurin@sha256:7a6e17f6335254a3e4340e9b990630f85e0810e979c136ba8df6f3f192451920
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256786027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942fd85c1d4eeedb9be4c99297d38532f3207e007ed5fbbb65cdf69625b778c1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 19:40:26 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 19:40:27 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 13 Aug 2024 19:40:28 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 13 Aug 2024 19:40:29 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 19:40:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Aug 2024 19:40:42 GMT
USER ContainerUser
# Tue, 13 Aug 2024 19:40:51 GMT
COPY dir:cf98fec7e439356342f3bf03fb67b0dac0e213296a20d5e427a9ebba9080193e in C:\openjdk-8 
# Tue, 13 Aug 2024 19:41:01 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee91db53edb9eaa638d7d926c33dc3d39a0bedf5ace2c9ff25f8c413bc3ea2c6`  
		Last Modified: Tue, 13 Aug 2024 20:30:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea35f7f090816a7fe5add0424cba285d8df77c18ec47c75e44a74608ef3a8573`  
		Last Modified: Tue, 13 Aug 2024 20:30:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65441e8750433f51ea383ecf14615ad0aeb32ac9a7a6007a17d4dad9992843f9`  
		Last Modified: Tue, 13 Aug 2024 20:30:04 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189cbb97da65c2c90ba3d40d62fa18d23f449c995650ca147be715f39f38674f`  
		Last Modified: Tue, 13 Aug 2024 20:30:02 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1772ece0bfed76416643ea51bbfb4d3151924b1f9d31132914a915edc2b125`  
		Last Modified: Tue, 13 Aug 2024 20:30:02 GMT  
		Size: 70.2 KB (70247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036c2827782fd0886f7e5607fde3d6236d41d825003869a02e2fcbe3bd66451f`  
		Last Modified: Tue, 13 Aug 2024 20:30:02 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf3347591e328ec8184510a1fdbcc3d32a22a4d869b5b9d78a4d48e8cd34d42`  
		Last Modified: Tue, 13 Aug 2024 20:30:11 GMT  
		Size: 101.5 MB (101544461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ac55a49244d850cc93ac337681b38b57f4b9d54b18a9383f2862003f4f7982`  
		Last Modified: Tue, 13 Aug 2024 20:30:02 GMT  
		Size: 82.5 KB (82524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
