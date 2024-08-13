## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:eaa39e1c4b665a69b0ae330d44119b085efb44c059dbba23ae9f762e84a0ce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull eclipse-temurin@sha256:92e909988e5b71f9e720cffeeed0b741393a2de1c95f5d076b7088e0c3fc3757
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195267586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563a1e0ebafc145db68326d729499fcac2c00861ae3b16f6b056b6046fc1c341`
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
# Tue, 13 Aug 2024 19:44:19 GMT
COPY dir:9cd76711a1e21cd053ac2280c0520b18fc7c9ba73d3efc8192b2b62cbbddbbff in C:\openjdk-8 
# Tue, 13 Aug 2024 19:44:28 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:f4840fa1c379496159b54cbe1d5e8384367b33ff9efbbf0d03f0794f5e22c289`  
		Last Modified: Tue, 13 Aug 2024 20:31:06 GMT  
		Size: 40.0 MB (40019023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9128131f245900d4b58163f6a09137fbcf00d274b6c0b82b0b7b2b872b56233`  
		Last Modified: Tue, 13 Aug 2024 20:31:01 GMT  
		Size: 89.5 KB (89521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
