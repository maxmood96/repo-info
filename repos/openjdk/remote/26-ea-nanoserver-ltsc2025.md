## `openjdk:26-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:f63d5b58e3d8a20351242116ea720a6048ac63f556bc6e51037990b640de7d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:26-ea-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:0b3e4e2e450859ef53b9c4a8cf898a80d13c847d5818a5963cca6003b74951be
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.7 MB (410706389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2861bc6801a5bcbf364f65df1a640adf7017b88440a445e5fc5482d26a20490a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Mon, 30 Jun 2025 18:15:34 GMT
SHELL [cmd /s /c]
# Mon, 30 Jun 2025 18:15:35 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 30 Jun 2025 18:15:36 GMT
USER ContainerAdministrator
# Mon, 30 Jun 2025 18:15:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 30 Jun 2025 18:15:41 GMT
USER ContainerUser
# Mon, 30 Jun 2025 18:15:42 GMT
ENV JAVA_VERSION=26-ea+4
# Mon, 30 Jun 2025 18:15:50 GMT
COPY dir:9343c399342bfceaf41d41506cae5b04cc1bd9723c9bec54f094b2ab7e5f9176 in C:\openjdk-26 
# Mon, 30 Jun 2025 18:15:57 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 30 Jun 2025 18:15:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fafcaf18cdaf69d3d8c820bd56c5a3d2c1d478ecc4b8bab53207a3fd48ffe5`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c23d1d89e4979f2e09e503f3765929b22fe03aa00e816ff7fec070228d08b8`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d8286f53a882d9bb52b1c7709e7b32149b7454ec23728884f9cde797fe39a`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec84a1c830bfccec928388db1bafa6cf3b5ee6a0ddb9bf6cf66a0b1e257848c9`  
		Last Modified: Mon, 30 Jun 2025 18:16:28 GMT  
		Size: 75.4 KB (75398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353873f9e92f12402a217afda63c1ad8bc4e0cd58b08273262d9b7cf327820c4`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2940a6cce1d4ac75088aa476005742ba1a48b71eaabc72a4656879d72582846d`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ddce15f3a3d8f23fb1e46569c2f2f8089b3fa01ec5d7167cf6e92c3144b0c1`  
		Last Modified: Mon, 30 Jun 2025 21:24:26 GMT  
		Size: 218.4 MB (218427850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42c71ed066dfe97158c83d30917e29416a15655a70afdb21b39a591f0fcd46d`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 114.3 KB (114297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108fea4f867f60c3289f7d2078aa07e82abd425b3f3d0463a74166245c3cd183`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
