## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:4c8dab32c4356964e55bd58318f12159f3f70e0b153fca255139634693ce9e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull eclipse-temurin@sha256:9fa0c60b211376f8394cf12c82776c539e91916a8626dfacb5618b32b206acfb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164267828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ae3bf6fb00d5f797e78262ba900e5479d565e38d05a5a3c53161381153a6e2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 01:20:55 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 01:23:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 13 Mar 2024 01:23:31 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Mar 2024 01:23:32 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 01:23:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 01:23:41 GMT
USER ContainerUser
# Wed, 13 Mar 2024 01:24:22 GMT
COPY dir:a9fc3c1ff9b46f8bdbd24fa63859ebc78303825dc025dc6f7e000bebb5265b19 in C:\openjdk-17 
# Wed, 13 Mar 2024 01:24:32 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e98336f720b829e374bd1d59306210d3700861b11d3df51506afbc0b50d039`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bfaafd714cfe6d656a777e25009d2c0940752258084af36bdd8ad744565131`  
		Last Modified: Wed, 13 Mar 2024 01:41:59 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abcfa255ba89192e7271d9a22b4a314b6efeda93800382c594b9c9dc9a5a1bf6`  
		Last Modified: Wed, 13 Mar 2024 01:41:59 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a89c1fbee62f675007c4ee4e602d7789f01acc5cb89a0bd057511ab275d21fd`  
		Last Modified: Wed, 13 Mar 2024 01:41:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9585bd42c22875a1867fddfb37242dba1d5115ed9b6e89b77c2451f562e4208`  
		Last Modified: Wed, 13 Mar 2024 01:41:57 GMT  
		Size: 78.2 KB (78249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f720ddc0afd0f358286bdadabbe6229c49427e4e99e0e43e04cb23c17c81767`  
		Last Modified: Wed, 13 Mar 2024 01:41:57 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b3083a3dfde85b2fbe2b7de9c24519b849a0b894753ef9ad60e269efd85e90`  
		Last Modified: Wed, 13 Mar 2024 01:42:32 GMT  
		Size: 43.4 MB (43420437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1441cc722a53aeda7e5b0c107faf2ed202706dc29e7ca5a9c0dabf2e598aa0a5`  
		Last Modified: Wed, 13 Mar 2024 01:42:24 GMT  
		Size: 60.9 KB (60917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
