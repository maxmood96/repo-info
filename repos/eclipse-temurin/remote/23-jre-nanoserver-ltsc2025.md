## `eclipse-temurin:23-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:df78b81e295e75c493e3edd484386ad3f91ee71de7e5298716dcb06a28c2a358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `eclipse-temurin:23-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:062306f973bceb7ae688d5e82d3022b54e5ea01e26185967ccde2d77b05c1547
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255044600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e07fe058c3d6af7c07db59e5bc24d13d3beef231fca563edabeb10daa203e9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:13:37 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:13:38 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 27 Feb 2025 19:13:39 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 27 Feb 2025 19:13:39 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:13:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 27 Feb 2025 19:13:42 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:13:47 GMT
COPY dir:f0b8f3d1970d52810d59047a7e1dfff98787b37140cc4aafc37fc86b09fa8be8 in C:\openjdk-23 
# Thu, 27 Feb 2025 19:13:51 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1972b20bd706211d38ad6a7019c45938907494fab5759ae8f9a26d6ec1f4a68`  
		Last Modified: Thu, 27 Feb 2025 19:13:54 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb406cdea18c2ec88d14e20338053851b4e3457dc2c9f34c6704d5b153d6cf39`  
		Last Modified: Thu, 27 Feb 2025 19:13:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f79b7ddde2fc01a4ad1d4c8d23f18341aa270905f0c3913a7e5967521688776`  
		Last Modified: Thu, 27 Feb 2025 19:13:54 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab4fdca0e3f87588f2a5e008a05aa7872567d2184e103d4be49e167d755028`  
		Last Modified: Thu, 27 Feb 2025 19:13:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0d6d1238aab00e2c11dd10a6c66f23f9bf6bc5413417a8b658d324b4c085d`  
		Last Modified: Thu, 27 Feb 2025 19:13:53 GMT  
		Size: 76.0 KB (75993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04591fdd334575d9ba173028debb95997c59453bded7e0f100afc8807a652b4c`  
		Last Modified: Thu, 27 Feb 2025 19:13:53 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286b2c6089fe22ea9982c82ca6b4fe3750d40d3d2b2fefa037e6145a18131ee4`  
		Last Modified: Thu, 27 Feb 2025 19:13:58 GMT  
		Size: 49.0 MB (48979629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37f8c1194745d55fb0d8d6fe5a0aef5925976ecae322209a83b7ed70b1d3c65`  
		Last Modified: Thu, 27 Feb 2025 19:13:53 GMT  
		Size: 93.5 KB (93479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
