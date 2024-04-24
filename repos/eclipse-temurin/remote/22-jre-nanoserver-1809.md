## `eclipse-temurin:22-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e6e9c6e5a89296822534ffce19c2002437774266a1984c43a03d0db0498f6683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:22-jre-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:6da5773d8b69d71f981613e1874d36c8acb1e38d50a5797c749a7d711e8cdf5d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156819387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded7d09b9ef5c03f84d101b63402f6a3e7a1f1627f1886be7f43ba0e46ca5bde`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:16:44 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 24 Apr 2024 19:16:45 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 24 Apr 2024 19:16:45 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:16:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:16:56 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:22:15 GMT
COPY dir:b356dfbfb05ab2ab46133b6b7ad4e4cb6a7442df8599937d6806166f02780fa5 in C:\openjdk-22 
# Wed, 24 Apr 2024 19:22:28 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99162cf301795a2934b58cb175b4b9bd833ba4ef022bdf311a3f5b6d4253f33`  
		Last Modified: Wed, 24 Apr 2024 19:44:34 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e333a85e4f99df6b7264ead3c9f8fc3447fc23c4a3283ca9a48b984c2213ed`  
		Last Modified: Wed, 24 Apr 2024 19:44:34 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92c1295a14273c026102afacdde9b5d3af241cc9b1e82084b9123fd995bf59b`  
		Last Modified: Wed, 24 Apr 2024 19:44:33 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cecf7884caa59b9e435973a173d2f68fcc934dc652a84735cd11fe9c51e8ed`  
		Last Modified: Wed, 24 Apr 2024 19:44:32 GMT  
		Size: 64.1 KB (64142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04fdbc0e3b8be01e12d59ba00b6ec0dcf8b86b227d058381f045173a941252b`  
		Last Modified: Wed, 24 Apr 2024 19:44:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028dd2e25fbdf916c4b2b1352db76dbf5f6c369e5a631f30f3211d4f0aee88b8`  
		Last Modified: Wed, 24 Apr 2024 19:45:57 GMT  
		Size: 48.5 MB (48487696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cd6916cf95a86dab65876b3556ea59030e0e1450160360385b36c8b6c4e9a0`  
		Last Modified: Wed, 24 Apr 2024 19:45:48 GMT  
		Size: 3.4 MB (3373161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
