## `eclipse-temurin:25-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:dab1ec83c9b6cf084e5278cd79801063ac25e525066cc89f205729c2176d3674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:978f905546f474efe3624fb27b21c612054fed5a5c8c52dcbe39a5352d771e1f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181417141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8caf3971d1adbd973b20bdec83b66dcaa99eced1ff59181cdfd092a6e9b042`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 08 Nov 2025 19:19:24 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:19:25 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 19:19:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 08 Nov 2025 19:19:26 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:19:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:19:33 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:19:55 GMT
COPY dir:38f2d146da8b2d45f6309f76e3864fba66a43ff9541e6e5522e91b15798552e5 in C:\openjdk-25 
# Sat, 08 Nov 2025 19:19:58 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55a25053d81be59768048737141f7bee543022838a62738b90b4e5b9f88bf91`  
		Last Modified: Sat, 08 Nov 2025 19:20:20 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7691e357710f83a6f4a10711c485cb2aef5beadf30bf29f0e60c7f7441b76a18`  
		Last Modified: Sat, 08 Nov 2025 19:20:19 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a24af416cc3814ec2ee9194b68a3b45f585de57c9ff3d048bd7f9eca7e772b`  
		Last Modified: Sat, 08 Nov 2025 19:20:19 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5cfd6a6b5589761cb1644987bb6fa86736b3e0f684bf2a5b088a0d8ddbdced`  
		Last Modified: Sat, 08 Nov 2025 19:20:19 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dddce623f763543befff1879dd0518f270f1f97bb09807c59d119cb0cbc1d0`  
		Last Modified: Sat, 08 Nov 2025 19:20:19 GMT  
		Size: 74.4 KB (74393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5083929a2fd28e0485c183a4c42376770ed848176a03a8aa82b73170824d8d`  
		Last Modified: Sat, 08 Nov 2025 19:20:19 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1790c07f8620789e7ae45c569bd601a485e594f972fb70aa321428550b34cadc`  
		Last Modified: Sat, 08 Nov 2025 19:20:25 GMT  
		Size: 58.6 MB (58563880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c8c9f71ed0aa5f1f26cb0ef7223344405d50b4e507c53a245b6786e16510fe`  
		Last Modified: Sat, 08 Nov 2025 19:20:19 GMT  
		Size: 89.5 KB (89469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
