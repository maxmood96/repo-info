## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:aae2576612e83338107413af1e975d34a1bf89dabfc987f17f8aac383cf9ad62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:e1e34c063aed3bfd513db3830db27e5455b0d6256bcfcf88c23831eefeec6089
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225167204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fb48250e939c2e9520d915958c22b1704febb5f8d30678f1b98e617138cd9a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Mon, 28 Apr 2025 20:56:30 GMT
SHELL [cmd /s /c]
# Mon, 28 Apr 2025 20:56:31 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 28 Apr 2025 20:56:31 GMT
ENV JAVA_HOME=C:\openjdk-8
# Mon, 28 Apr 2025 20:56:32 GMT
USER ContainerAdministrator
# Mon, 28 Apr 2025 20:56:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Mon, 28 Apr 2025 20:56:51 GMT
USER ContainerUser
# Mon, 28 Apr 2025 20:56:56 GMT
COPY dir:5c4bbf817a67c787f7f2d8809dee99be16882c3512e063f4e47205ca5ccbd190 in C:\openjdk-8 
# Mon, 28 Apr 2025 20:57:02 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cf67c141e0bc82faee48ffd4718e1f9990f4d2e5b13242db35765ac56d2dab`  
		Last Modified: Thu, 08 May 2025 23:34:44 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70b4868e1dd8486c17c42535df8303838f2f20297b85ae7dd17440f888f26c0`  
		Last Modified: Thu, 08 May 2025 23:34:44 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047c545938e86fc6ec2bb1c3ac896427b73902c91113e4a08ed8c8c2e2f44bcb`  
		Last Modified: Thu, 08 May 2025 23:34:44 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510649d3104fa930e065f9c1590f6d537c74f99b981f3d3d74069ad98858b4e8`  
		Last Modified: Thu, 08 May 2025 23:34:44 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27536436d463488f7aa3db250c048b63e93c8bd9001201c91307b09ff41a810`  
		Last Modified: Thu, 08 May 2025 23:34:45 GMT  
		Size: 84.6 KB (84615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240e537422357d06571dacbd8a439206c9ef564c3e16e2da9e53dc55fb69dabe`  
		Last Modified: Thu, 08 May 2025 23:34:45 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af4016f5da48cebc9711ed36d942e34a1fad17c04598cde8629b4cc3f1f9451`  
		Last Modified: Thu, 08 May 2025 23:34:50 GMT  
		Size: 102.4 MB (102440001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ac8ebb4a4a375566385b13934edbf3c6f4e2a69e99fa9145480d754542f70a`  
		Last Modified: Thu, 08 May 2025 23:34:45 GMT  
		Size: 98.2 KB (98248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
