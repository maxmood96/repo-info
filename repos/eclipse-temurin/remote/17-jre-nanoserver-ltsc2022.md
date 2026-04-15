## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0e2099b584b3af20e78d35702e2de06defaa314e4be6c03f88bf49497b8e8e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:1995d9e0b542a5fd5515327b474cb2d202f6922de3252ad61b6d2a63d7080e84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170947093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3671ef1cee53d6bef1fb053d6c1b04492162ccdec55b6b2c7f4018a134ef7a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:11:19 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:11:20 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 14 Apr 2026 22:11:21 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 14 Apr 2026 22:11:22 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:11:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:11:31 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:11:47 GMT
COPY dir:064fca0b30194d02fe341355ba6a62fc1748c82418561395eb5bec357779f4c8 in C:\openjdk-17 
# Tue, 14 Apr 2026 22:11:51 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a92e0e44c72d10bf75d0edaa06ddcc97f14d6c2afb302cffe065c90d3dee37`  
		Last Modified: Tue, 14 Apr 2026 22:11:56 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f198d6d9254134cda4b5d65b21550b5eac18e2f99d25f209c0963a5e75298b5e`  
		Last Modified: Tue, 14 Apr 2026 22:11:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1e6523db694c58f11c29a80b28fb8ef4b6c6e1acee4f9f6d9692451b4f7c53`  
		Last Modified: Tue, 14 Apr 2026 22:11:56 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275a4de88418aa0f8f32ee3178ce65dc25c6567a94f2e15cbe09dc455c10f77c`  
		Last Modified: Tue, 14 Apr 2026 22:11:55 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87513a9b183eed63477b58ee877b9d1290d8cb46f350f4a258cfafb6bb41308`  
		Last Modified: Tue, 14 Apr 2026 22:11:55 GMT  
		Size: 72.6 KB (72634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597e113d469012e96af200f6302c86f2b2e0f6461e97ffdc5880b4412097b75b`  
		Last Modified: Tue, 14 Apr 2026 22:11:55 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758e6d01dd1bcc5f05d3f4cb50265a373f6ea07e8b9380c9cd4b5836c4a506ce`  
		Last Modified: Tue, 14 Apr 2026 22:12:00 GMT  
		Size: 43.8 MB (43794732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f977a275cd7d58255d589d1a2995a52c2d2949a90dd494164b43254fb497d980`  
		Last Modified: Tue, 14 Apr 2026 22:11:55 GMT  
		Size: 118.4 KB (118438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
