## `eclipse-temurin:21-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:68000ff52b91db13e1b578cefc34622e695901912f0018db1947490ef644e58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `eclipse-temurin:21-nanoserver-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull eclipse-temurin@sha256:c67eac49df28bd9b9561e7420213497ba09e7666c1c082bc49b39eec4d59f7f5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321488350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babb9eb7ac3ce9eee58ecb39e5ec8b4eb53c84d260fd42d9ffb8c29a6b9e7c98`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 Aug 2024 19:28:00 GMT
RUN Apply image 10.0.20348.2655
# Tue, 13 Aug 2024 20:19:48 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 20:22:59 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Tue, 13 Aug 2024 20:23:00 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 13 Aug 2024 20:23:01 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 20:23:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Aug 2024 20:23:08 GMT
USER ContainerUser
# Tue, 13 Aug 2024 20:23:22 GMT
COPY dir:a4ffd7e89e4f3b2e7536e802b1dd43338b71e63559dd6ffcb51f99d655bc67fd in C:\openjdk-21 
# Tue, 13 Aug 2024 20:23:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Aug 2024 20:23:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:695cae91f2de8dadf81c8b3a95f4942533ef064a72ad8fa7843cca84a839bfba`  
		Last Modified: Tue, 13 Aug 2024 20:02:51 GMT  
		Size: 120.6 MB (120554921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8146ec246b230c09f8b628d688c831ad1269b9cef24c5c95a8d1eb2f76b89bdc`  
		Last Modified: Tue, 13 Aug 2024 20:40:03 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35338625971a9b9199a2f1cbe20401827cd241ab5b30520723b78338dd73120d`  
		Last Modified: Tue, 13 Aug 2024 20:41:57 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f68712be27c7f26f43fd490a584e62126aca1a405c29d048a3b8872d5b676e1`  
		Last Modified: Tue, 13 Aug 2024 20:41:57 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11cce6f6efa5c8dfb2624dcef38e6991b67cd974a979a42087d3930db6d13303`  
		Last Modified: Tue, 13 Aug 2024 20:41:57 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9605e6fe1584a1d8b77aa3bf20c2e65ed4b25d50af3ebd686998879b8bd7a1`  
		Last Modified: Tue, 13 Aug 2024 20:41:55 GMT  
		Size: 78.7 KB (78655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5634e0477def673635de3f25a298e17bd1493413467c10c4fbe1f43664433b5`  
		Last Modified: Tue, 13 Aug 2024 20:41:55 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd20bcea29e8a82002c2a2dc54911c63749257c62789776010ebefc06fd908e0`  
		Last Modified: Tue, 13 Aug 2024 20:42:10 GMT  
		Size: 200.8 MB (200777390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f913f6eea6971967f06c6a4ba189002630a91fa804a5998d1c42479f41bc38de`  
		Last Modified: Tue, 13 Aug 2024 20:41:55 GMT  
		Size: 70.7 KB (70698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66e99f2c93a4481be307570e64095717971a66229b56320b50bd31293e1d68f`  
		Last Modified: Tue, 13 Aug 2024 20:41:55 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
