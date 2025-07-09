## `eclipse-temurin:17-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:6f49445db712295f806ca3d0978197d14b4319a557e7546163cb83c8c6b13f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:fea0e1b252b1dbb247bc8341a23ba0632ae402bc4c96336553a31ec6394522be
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 MB (237071024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec68d1eac55f478220af3f1dd31df9997bb9d87102d8979e4c684754519f073`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 18:13:07 GMT
RUN Apply image 10.0.26100.4652
# Wed, 09 Jul 2025 19:15:32 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:15:35 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 09 Jul 2025 19:15:38 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Jul 2025 19:15:42 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:15:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:15:55 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:16:03 GMT
COPY dir:6f6fcea1890c098492beafa1d6f550d144651035b2d4a098a7658e545737cf82 in C:\openjdk-17 
# Wed, 09 Jul 2025 19:16:10 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2fd4507679915420227c89c4f57165747b37deaa62748936e2af8c2f38de0b4e`  
		Last Modified: Wed, 09 Jul 2025 01:51:41 GMT  
		Size: 193.2 MB (193150329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8132e8fddc7bb3724b5b3b38d3743a9e00be55af99f848215ba90c403f6d0094`  
		Last Modified: Wed, 09 Jul 2025 19:16:40 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d85c704671f7d894843830dcc4dda9d7123b6015d84155b3d00dad6b945d2e`  
		Last Modified: Wed, 09 Jul 2025 19:16:39 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468a11325518799272a59158ba2a10c83c820dedbb485a084dfb420cfa82cb7b`  
		Last Modified: Wed, 09 Jul 2025 19:16:40 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3494b32921ac8b9cc7ab51755e63744c26f2c62e505a3a0bd0e86354c9e6b6`  
		Last Modified: Wed, 09 Jul 2025 19:16:40 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1574b3a65bd3b5261b61015151e5b7373b38284eff9665c5b3211fb26756b0`  
		Last Modified: Wed, 09 Jul 2025 19:16:40 GMT  
		Size: 83.3 KB (83346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90aeeb81bf77b017452fef03ca70121b7adeddf8de3ff3f469ef3af88807b32d`  
		Last Modified: Wed, 09 Jul 2025 19:16:40 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9cc40ec388a6478a1c613181180a8ecb4be1ceac22198632b22e4c7bd83504`  
		Last Modified: Wed, 09 Jul 2025 19:16:43 GMT  
		Size: 43.7 MB (43736718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39c58524586b71393bff84201ee6481952293cec9fc3b4ee9e5888b24f588d7`  
		Last Modified: Wed, 09 Jul 2025 19:16:39 GMT  
		Size: 95.4 KB (95359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
