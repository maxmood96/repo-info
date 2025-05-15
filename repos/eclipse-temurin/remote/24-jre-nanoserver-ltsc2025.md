## `eclipse-temurin:24-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:ef4cc98b02cc0e1e68c88a597a699f72b460ee8fede3333c3899378fe85d53d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `eclipse-temurin:24-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:fbd0f99b32a0c5c3165f775ccdb324b110c92e2b4fe1f25baffd96d1ecee9d0c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249309484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993998e88a593750200af2f9723eedc1328293f94bcd485119f57653e643f964`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:14:35 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:14:37 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 14 May 2025 21:14:38 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 14 May 2025 21:14:40 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:14:47 GMT
USER ContainerUser
# Wed, 14 May 2025 21:14:53 GMT
COPY dir:ad5bc1bf6efc16ac6d52d57c1c7046f6f9b2ef9ef08387497ec457eb9554ce7d in C:\openjdk-24 
# Wed, 14 May 2025 21:15:00 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112604d6a727fda1f20e95c19a1745a4244b16f4ddda6c3898bbfded3f8156a6`  
		Last Modified: Wed, 14 May 2025 21:15:05 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee1793b60d3dbacfc48fa861a0f7d6d6fdab176c76554bfc3d06538577739ab`  
		Last Modified: Wed, 14 May 2025 21:15:05 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd95f8a0c9b9afaef4bb15c6bcbcfa4a09b351a25b0182b839ecbb4cd6a9a189`  
		Last Modified: Wed, 14 May 2025 21:15:04 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac91b8f4f128cbed4ad806ee3d2ee1e0167bb6919d69b499b3ccc6aa809da66`  
		Last Modified: Wed, 14 May 2025 21:15:04 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ac58c5c589c976b6cfb570a30d998afa81ea0eb9e17929369d56782aaae63c`  
		Last Modified: Wed, 14 May 2025 21:15:03 GMT  
		Size: 77.9 KB (77934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c3da540a8528f859e9afbd9dc9d82b95b67a1e7d8c4232be38f6708498094d`  
		Last Modified: Wed, 14 May 2025 21:15:03 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26516979b5ab0ac56f261846f5cdf59da34d4993ae25a31bc5cd83f4f0e7557`  
		Last Modified: Wed, 14 May 2025 21:15:11 GMT  
		Size: 57.7 MB (57710152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b89262b20c1247816984c3fdbb5fc41cbab3312f8df249a09f3424d646ebe88`  
		Last Modified: Wed, 14 May 2025 21:15:03 GMT  
		Size: 104.1 KB (104112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
