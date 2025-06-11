## `eclipse-temurin:24-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3a9d0be85951f8ce059e0008dfe6a00562b824d2c0541013c4cbc67517d97f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `eclipse-temurin:24-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull eclipse-temurin@sha256:f44002b4e6420ee51f890362a0d8439c4cdf7f98dcaa68a0aa87bdc67b491afe
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180429995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74dfa01a809a8b24f5ad4ea85dc65d8a851e2b3979e2699252f65019cf31f46`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:19:02 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:19:02 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Tue, 10 Jun 2025 22:19:03 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 10 Jun 2025 22:19:04 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:19:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:19:07 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:19:12 GMT
COPY dir:ad5bc1bf6efc16ac6d52d57c1c7046f6f9b2ef9ef08387497ec457eb9554ce7d in C:\openjdk-24 
# Tue, 10 Jun 2025 22:19:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b82daf28d6bf24fb4eaf4cbf7a3fea424e8d3ab9daab911cfe76d259cde18d9`  
		Last Modified: Tue, 10 Jun 2025 22:19:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e6be6007a2b6127d62f56b0e60ed1fdd4c5e64ee6e3c7d1f3932ef95ba8a91`  
		Last Modified: Tue, 10 Jun 2025 22:19:56 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8dbd4b916c5b9a2aa0db40b630fa9c6a073329cfc82b7de47163391e67ff4f`  
		Last Modified: Tue, 10 Jun 2025 22:19:56 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b21346ef461f559bf0e75d148a4019bf9e2a323ee8249d02accbb9ff7ac34cd`  
		Last Modified: Tue, 10 Jun 2025 22:19:56 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c722d6e42a738ab92780584138350b0b72edcb9105855279f8e4853e10ca8cc6`  
		Last Modified: Tue, 10 Jun 2025 22:19:57 GMT  
		Size: 79.0 KB (78964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d44a22d5aca670dcd3296ee7f919e4cd72c8bde4552d8290e4d77c66602fad7`  
		Last Modified: Tue, 10 Jun 2025 22:19:58 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb262a593a2d02b1db0a69ecd44fe3255fdcd72f8073b9b9b3318756498db35`  
		Last Modified: Tue, 10 Jun 2025 22:20:03 GMT  
		Size: 57.7 MB (57709065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2cf47812ff778640bd81c4f748c0efceb7c5985dc7fe31f30260590aca31aa`  
		Last Modified: Tue, 10 Jun 2025 22:19:58 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
