## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:9a98c43c7a190db6617903ecc7226f35c32914690065422ea83646f032722e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:04b35499968145d5ef58140b415d8963b32042c0aa3458dd8bb1ddaa755e0ac9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245942931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d537e6c4120735d440856378c8d9cba27f36d3d6ce66efe9f6ab7a29cecf024e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:18:08 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:18:09 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 09 Jun 2026 23:18:09 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 09 Jun 2026 23:18:10 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:18:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:18:12 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:18:26 GMT
COPY dir:4940aac187beb0c950977243d0b1d703fc0231f7cabe77dd307cf1e9c831ffc7 in C:\openjdk-21 
# Tue, 09 Jun 2026 23:18:30 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee5a15e6c0ae33d8458f16b5e982a3e6eb3be95d54d8918eb8862671f3dd652`  
		Last Modified: Tue, 09 Jun 2026 23:18:35 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb22b40ceed07a656d6909841ba5c76339ce307eec296fa43701d88806d07aa3`  
		Last Modified: Tue, 09 Jun 2026 23:18:35 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09945c36987cb0d86f3de1bd5694cfaf169665eb3699bd3bd7c95e3dcefe4479`  
		Last Modified: Tue, 09 Jun 2026 23:18:35 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea1ac0b3c8207acb6bbb4a92cc44621895d2cec125486c0d6f4972bfc7368db`  
		Last Modified: Tue, 09 Jun 2026 23:18:33 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0977cf5f56a0dd837a79918db0080c5e0e33fcc42753a1421d14abdba8a591d`  
		Last Modified: Tue, 09 Jun 2026 23:18:34 GMT  
		Size: 73.2 KB (73177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad062f42492fe3da2d38051d6ea21022b83752ef1bb950a7c3e34bf8f27283ea`  
		Last Modified: Tue, 09 Jun 2026 23:18:34 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2250f889d79e8f71552c89da532b2177b4787a6ae7f8a650241a038d98096b45`  
		Last Modified: Tue, 09 Jun 2026 23:18:40 GMT  
		Size: 49.1 MB (49082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4ea58134ffffeeda403f0d8db01380870d52b6e3cab9f44a1a34a9f7fe64e0`  
		Last Modified: Tue, 09 Jun 2026 23:18:33 GMT  
		Size: 113.7 KB (113650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
