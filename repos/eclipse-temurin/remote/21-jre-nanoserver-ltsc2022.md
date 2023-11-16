## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:596e0aa54ea513064709465e6755a3a491f3e61a77b8a6caba9a94bdfb0f935e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull eclipse-temurin@sha256:52a90fe4c29ceddcfaf9af0616e869cdc549482be1d578f1a6c2c15f6a370a1d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169587545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4324d3fe2965d84561f15d7b203e3d8c19b985e5c3e7929890a1009dc1589620`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 06:09:19 GMT
RUN Apply image 10.0.20348.2113
# Thu, 16 Nov 2023 02:17:18 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 02:21:27 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Thu, 16 Nov 2023 02:21:28 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Nov 2023 02:21:29 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:21:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 02:21:41 GMT
USER ContainerUser
# Thu, 16 Nov 2023 02:22:28 GMT
COPY dir:a5a397b00294543a7015e10bed54514e1c5f8af5ed3eff5933ba2b604ae103c1 in C:\openjdk-21 
# Thu, 16 Nov 2023 02:22:40 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:1ca4fbe907f22e883670decfa8d7f4490a79a995bb83a6c286248c21d61a62f5`  
		Last Modified: Tue, 14 Nov 2023 21:13:36 GMT  
		Size: 120.8 MB (120753560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2f0edb58e1876347bbad88c907697db94e172aa6ff4a38560ccfb68d72aa86`  
		Last Modified: Thu, 16 Nov 2023 02:37:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d38c761f22514cb74d62a362aaceaff5643e34635a1a205276b38a73369c4b0`  
		Last Modified: Thu, 16 Nov 2023 02:40:14 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc6362d58554adddf75c17e64c65c7b198ae1bd1c13586007a811be2a76bac9`  
		Last Modified: Thu, 16 Nov 2023 02:40:14 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a189975ca6a65bd0bb69aa62ade1d685a91b9cd3b00370016b814c89109f24b6`  
		Last Modified: Thu, 16 Nov 2023 02:40:14 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a1e989bea1378ebde2905b30edb6311c06cfefa79673c6cbefbe0c1d4e073b`  
		Last Modified: Thu, 16 Nov 2023 02:40:12 GMT  
		Size: 78.9 KB (78886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740931fbe3e3d4b7f0e8347e60522d74ea0b079c2bca51844161f8336c7d8b6`  
		Last Modified: Thu, 16 Nov 2023 02:40:12 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13ee9011ae798c3a3c625c95d6dae1404331440edeb00296b597c0f380249a1`  
		Last Modified: Thu, 16 Nov 2023 02:40:55 GMT  
		Size: 48.7 MB (48688702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d5232e056b924dcad0cc8a7abe45c4d9558a392ee6df61654173678329b8`  
		Last Modified: Thu, 16 Nov 2023 02:40:46 GMT  
		Size: 61.1 KB (61118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
