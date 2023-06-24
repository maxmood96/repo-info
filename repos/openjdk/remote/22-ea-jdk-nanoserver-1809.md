## `openjdk:22-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:6c0303405e30fdf86f0d74cd5dc2c38916de30aeb9794d977a95c4c1f7757c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `openjdk:22-ea-jdk-nanoserver-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull openjdk@sha256:0bdee696f3d6ebb941723e1021b70fdf0088a21de32740009e31b8fb9220b40f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307042675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a6467dff2acc413497f6402c5d0d111c44979dd78395a27807702a9e0b49bc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 21 Jun 2023 07:40:33 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:41:51 GMT
SHELL [cmd /s /c]
# Sat, 24 Jun 2023 03:06:42 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 24 Jun 2023 03:06:43 GMT
USER ContainerAdministrator
# Sat, 24 Jun 2023 03:06:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 24 Jun 2023 03:06:52 GMT
USER ContainerUser
# Sat, 24 Jun 2023 03:06:53 GMT
ENV JAVA_VERSION=22-ea+3
# Sat, 24 Jun 2023 03:07:08 GMT
COPY dir:8a420f20927ee12c5664336246fe9e7981c10034572e95cbd352de42199c9295 in C:\openjdk-22 
# Sat, 24 Jun 2023 03:07:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 24 Jun 2023 03:07:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:09087aac643f57e5e24f95fe0a1c8519d0f93dfcf4500263516c0f3874290109`  
		Last Modified: Fri, 23 Jun 2023 02:23:11 GMT  
		Size: 104.4 MB (104400893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09be2e47b3dff420361e93d34eaadedcfd9549c9be5bd77936370792babf874`  
		Last Modified: Sat, 24 Jun 2023 01:24:43 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0720397410cf27e11864dcfc2c9afadd7f7b2969f2bf4a2fd452cc3c6fdb541`  
		Last Modified: Sat, 24 Jun 2023 03:13:44 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2871b71eb8c2564d7544ebac7d7abbfc1ddd2570586a73f216323cab124eedc6`  
		Last Modified: Sat, 24 Jun 2023 03:13:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3912e3db7b6050feb04d0a6219277fd3a5cfb6649ccd27fe845538d11da2ec50`  
		Last Modified: Sat, 24 Jun 2023 03:13:44 GMT  
		Size: 68.8 KB (68757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57de6a9e2121836773f8d9f7079a0c6aab28ae6275690ecdee66946d9a774c6e`  
		Last Modified: Sat, 24 Jun 2023 03:13:42 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6134d59b3e9a5db53f2125b3dc7b4abe29d68537f783495e092fef4df968cb7d`  
		Last Modified: Sat, 24 Jun 2023 03:13:42 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c95acfca2a5d430f6cb36cf9f344ff146f3afc1be69994e3580dd07b9af8cdc`  
		Last Modified: Sat, 24 Jun 2023 03:14:02 GMT  
		Size: 198.8 MB (198761042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73516fd26cc458e75c2561573b08646c65ffd41372a0e251fc94ec200f310fd8`  
		Last Modified: Sat, 24 Jun 2023 03:13:43 GMT  
		Size: 3.8 MB (3805593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0f0eb5bdfba36572511ced7a43f5374e8035de967800a6277c3a6ab2bd3746`  
		Last Modified: Sat, 24 Jun 2023 03:13:42 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
