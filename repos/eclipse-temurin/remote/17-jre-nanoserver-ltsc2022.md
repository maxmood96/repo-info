## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:835d236c1cad5f12e0adaadd707ca0bc277a46f83277289f506e343d0abc5a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:8bf193ce949118985972ba0392f147847eb942ac86803b704144c39785638bff
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165201019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3f6763a287f24d974f3366b4b98fb57f0781007a9c76d8260c02a587623f1a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:02:53 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:02:54 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 15 Jan 2025 18:02:54 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 15 Jan 2025 18:02:55 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:02:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:02:58 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:03:02 GMT
COPY dir:4c6d77ca6f58a330005c5f34389fe1882335ea3db28c021259e868cb18ddb756 in C:\openjdk-17 
# Wed, 15 Jan 2025 18:03:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4d29108397aca2ced9e82c7472f62b59cae237c95493a87155f6476583b715`  
		Last Modified: Wed, 15 Jan 2025 18:03:09 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce9f49e577e478b8dbbf49d128f13c199971c187f6832844ada7f6159716a3d`  
		Last Modified: Wed, 15 Jan 2025 18:03:09 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4bde282325e6cae63c53e3732183e6f05bb8b7111ba6f59a1c28efb07e2fc2`  
		Last Modified: Wed, 15 Jan 2025 18:03:09 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1d30ca96bd18f94976788281a6da6a9043d84ff151f0a747f5c4140d0ebe31`  
		Last Modified: Wed, 15 Jan 2025 18:03:08 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1f294065c5a5cf454e83fefefb0c431f6be5b7112c87d6930dae97737c37d2`  
		Last Modified: Wed, 15 Jan 2025 18:03:08 GMT  
		Size: 78.4 KB (78367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf16f89e411ca829a1d13b8fcc08e49ab2653de56694a821f21686ce8cd0037`  
		Last Modified: Wed, 15 Jan 2025 18:03:08 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4a06275e440b6f1d623c1ae8e5d58523e5361ab5b056d3b1c6433b61b4d0d9`  
		Last Modified: Wed, 15 Jan 2025 18:03:13 GMT  
		Size: 44.4 MB (44358919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35706c5451bbdb6b3310eb835ebb7ce5bc9d3e59317c47feca2586bcbce542de`  
		Last Modified: Wed, 15 Jan 2025 18:03:08 GMT  
		Size: 97.0 KB (97041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
