## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:07206f9680c881c5debeeb82d76ee3328ac0c629637e8d4b9629ee5f8227089f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull eclipse-temurin@sha256:ac02bc2c0660d814aa5edbdde812bc39cccbdd94956b433348ba1cbdddfe9a0a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314357242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f09f4548dd25b1f78416ffc357affaaff2528d403cfe5ee82a1a12d0e486b2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 Aug 2024 19:28:00 GMT
RUN Apply image 10.0.20348.2655
# Tue, 13 Aug 2024 20:19:48 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 20:20:46 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 20:20:47 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 13 Aug 2024 20:20:48 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 20:20:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Aug 2024 20:20:55 GMT
USER ContainerUser
# Tue, 13 Aug 2024 20:21:10 GMT
COPY dir:b5e9d6d7234e205f01359f52140171f1743cc309a4dc5e4224755ced7d18fbfc in C:\openjdk-11 
# Tue, 13 Aug 2024 20:21:20 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Aug 2024 20:21:21 GMT
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
	-	`sha256:7e4d702d09964f58a74605ef70f3bbac3f639bce491371021adcb4d2b4431a18`  
		Last Modified: Tue, 13 Aug 2024 20:40:42 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98cfd66c50a25e90135d888df9f5e21b476aa1da805b29d0921ed4a07ce1bef`  
		Last Modified: Tue, 13 Aug 2024 20:40:42 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183fbd712a963e52e7d253d6f5a82c3839adf9587bdfdc2de59a66b9e0a7612f`  
		Last Modified: Tue, 13 Aug 2024 20:40:42 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab1922c39f4c578f7dd56e6ecfbd28b0d148e6de4f7d04f37b8230cd28c101e`  
		Last Modified: Tue, 13 Aug 2024 20:40:40 GMT  
		Size: 77.3 KB (77277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624139632c148578ac7f39ac34ca86fc98cf280b210ba99f2df91bdcb1c565f8`  
		Last Modified: Tue, 13 Aug 2024 20:40:40 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b0446a85d30d3b4d246be524af13adddcc1d91c2a528bcff5655aee9c54f61`  
		Last Modified: Tue, 13 Aug 2024 20:40:53 GMT  
		Size: 193.7 MB (193657230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb395ee685db36f572ec0b5d64f13f7ddc3610002f26c70795641a3fad90671b`  
		Last Modified: Tue, 13 Aug 2024 20:40:40 GMT  
		Size: 61.1 KB (61105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0cf6d06483e5c5c6832412062ab7ba794f334759ea0259c587985cd1e4f5d7`  
		Last Modified: Tue, 13 Aug 2024 20:40:40 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
