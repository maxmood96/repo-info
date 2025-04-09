## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:982d6d46ecd5369c4773c997bde05359d57cfed5a0d3e1aa0d82847bb3ba4a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:2883c1e45a1f3efe744762baf054e46d045ea544219665d5297f1722b75db316
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239228880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd52d1e81c5e42054b29c4d9aa6307503c57b87cd36f6f801665fd14a28e0fc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:17:58 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:17:58 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 09 Apr 2025 01:17:59 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Apr 2025 01:18:00 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:18:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:18:03 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:18:07 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Wed, 09 Apr 2025 01:18:11 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01399613f2c93f045104a55047ac020d1c85f721bccb9770a01b50c8a71c01d3`  
		Last Modified: Wed, 09 Apr 2025 01:18:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef0f99b87da67075440ff4b47430d7c7b9e2132e3526443a8403f15c92acbc2`  
		Last Modified: Wed, 09 Apr 2025 01:18:17 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a17943be4be3c6267dcc1c4eb4c9e89bc8c235fdd6a4cc742b81257fae6a5d8`  
		Last Modified: Wed, 09 Apr 2025 01:18:17 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a038192a4d762b26824c222869b6e476edb5bbe41eaa2c5b29e47873893d13f7`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72af05e7dea4a3c392be36a9328a6a91e8863e3f36f844ebc5d9d05eaa83a9a9`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 76.1 KB (76123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf952cd3aedcf96015490c0f5136d177846f265e79b1c2d11748bf7d749e6e3`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044212d0f5f2731209febaeecdb648571e60b46e8fcbc1cf80d96d8f6c82a994`  
		Last Modified: Wed, 09 Apr 2025 01:18:21 GMT  
		Size: 48.9 MB (48940549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a11761655603bfc285b6cbcdab2d639912342a7a28f90307ef1dcb51025f5b`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 93.8 KB (93773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
