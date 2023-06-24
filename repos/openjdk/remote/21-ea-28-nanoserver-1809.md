## `openjdk:21-ea-28-nanoserver-1809`

```console
$ docker pull openjdk@sha256:7a5f440dc518696176423bf539ebe94ba63f184611280237ef16413933096f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `openjdk:21-ea-28-nanoserver-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull openjdk@sha256:928ce5745d12cd0589f314b29a846681d0db5dc711eb829719c2b9fc300e1759
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306229621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b391df147396c34a1bfb7873762af339e352c8a8ee224d2b274a1968c1624b8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 21 Jun 2023 07:40:33 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:41:51 GMT
SHELL [cmd /s /c]
# Sat, 24 Jun 2023 03:10:41 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 24 Jun 2023 03:10:42 GMT
USER ContainerAdministrator
# Sat, 24 Jun 2023 03:10:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 24 Jun 2023 03:10:52 GMT
USER ContainerUser
# Sat, 24 Jun 2023 03:10:52 GMT
ENV JAVA_VERSION=21-ea+28
# Sat, 24 Jun 2023 03:11:07 GMT
COPY dir:5e5e1336ec2d60e8b2707494abc1e5b87c4f17d59c6e98aa6bc368a25f065267 in C:\openjdk-21 
# Sat, 24 Jun 2023 03:11:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 24 Jun 2023 03:11:21 GMT
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
	-	`sha256:1761082022ac41b0f9e56c60b660a94c5cc48216abc4ee6585d75e5f639b8b83`  
		Last Modified: Sat, 24 Jun 2023 03:15:39 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d43ae3625180a30ce5075af37248f9b8bfb36b35d98ea87e0c69dd6309c66`  
		Last Modified: Sat, 24 Jun 2023 03:15:39 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7bf66e4a671426e237a857427cbba03c02b51ed5e66b0d72fc65d78ec04f91`  
		Last Modified: Sat, 24 Jun 2023 03:15:39 GMT  
		Size: 67.2 KB (67224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68960e43d220da8539c1fcad0e31945a1a70a4be19f3182a2d989413baa9e212`  
		Last Modified: Sat, 24 Jun 2023 03:15:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46134e04856756837089adf8bc5b38f23b1940101c8843dd8911209078b0419f`  
		Last Modified: Sat, 24 Jun 2023 03:15:37 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f936bb4f6d924c3b7eea7cec01cfc66f9054a2170c7ee5eb557a38f15306d32`  
		Last Modified: Sat, 24 Jun 2023 03:15:57 GMT  
		Size: 198.0 MB (197952142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc520ee82e14bade1b67b1915c98c2faea0ad12e3c8a9f24d7fb44ac5dba37b`  
		Last Modified: Sat, 24 Jun 2023 03:15:38 GMT  
		Size: 3.8 MB (3802429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a54cf5530a52a2244a9225aa68404d7a20ec1a8f66609f6b3fd44da0fa971e4`  
		Last Modified: Sat, 24 Jun 2023 03:15:37 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
