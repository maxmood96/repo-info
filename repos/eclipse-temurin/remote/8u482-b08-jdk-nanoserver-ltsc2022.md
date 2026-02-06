## `eclipse-temurin:8u482-b08-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:4d62241448801b3dfe9311c80c1463f9bca13619c491699f8d5e70be2305dbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:8u482-b08-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:5e7be784dae374609082b3dcd40a635aa65a447d3235b5b4577f8f717ac29f46
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228769705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bdc89f3ed660762403a5ed142cafc1bffa2333e1cf8ad54ee4eb981d696fd9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Thu, 05 Feb 2026 22:39:17 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:17 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:39:17 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 05 Feb 2026 22:39:18 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:39:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:39:23 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:39:43 GMT
COPY dir:076949d8a0679d24528f11c4150b1ea7a552717f0bf1fb11a9fa610f7e5e2ea0 in C:\openjdk-8 
# Thu, 05 Feb 2026 22:39:45 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81eeb53037f4a6db66b71a97aead342992cc6906094403bd195c8563fb7f71a4`  
		Last Modified: Thu, 05 Feb 2026 22:39:51 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18259b408b9e6abedaaf14b3c74b33eb9cbd67a8142bc3fe34c9c7544fd742a`  
		Last Modified: Thu, 05 Feb 2026 22:39:51 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54078bd55b717aa060c6295137d0052927e4396fc9b24469ae53cb52b436dc5`  
		Last Modified: Thu, 05 Feb 2026 22:39:51 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f28901147286fc2d96f4950dc07fa7d1af2edb717b791a95f8027c9a9005ff9`  
		Last Modified: Thu, 05 Feb 2026 22:39:49 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3628301e89c1cb278d69f4ba1942b1c7587c90e9a068fa26336d015caa314366`  
		Last Modified: Thu, 05 Feb 2026 22:39:49 GMT  
		Size: 70.8 KB (70827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6004d0afb2389eacbdd5e2eb9e5c7ba3ad3e271e4e3e810abbf13c55f24d75a3`  
		Last Modified: Thu, 05 Feb 2026 22:39:49 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745bc1437a04966f93a8791fe77b7ffdff243a89d8c9513390b715e80cac2739`  
		Last Modified: Thu, 05 Feb 2026 22:39:57 GMT  
		Size: 101.9 MB (101907973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f8f060b3c4ac1c7756427971482627004341144795b5d05887e856b6cf9345`  
		Last Modified: Thu, 05 Feb 2026 22:39:49 GMT  
		Size: 88.8 KB (88800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
