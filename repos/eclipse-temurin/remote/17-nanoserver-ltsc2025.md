## `eclipse-temurin:17-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:7799e0762ff8624fbd5a71dcb24df5620652d2f1cb2aad07253738ac2d76eb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:17-nanoserver-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:23fc5f26ce58e77d4cc06b417751bd2d103ecf22df993cd85ee6d2f8a19895b2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.6 MB (377555305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c9d3746be5312902e89ad14608e0d9520e35db625ed1d77dc23c7a9b893425`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 02:17:37 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:17:39 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 09 Apr 2025 02:17:40 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Apr 2025 02:17:42 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:17:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 02:17:48 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:17:57 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Wed, 09 Apr 2025 02:18:06 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 02:18:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd84ea8fa4cf92a3ae904ce31733a57eb368d717a2b233a983fcf05567d595e`  
		Last Modified: Wed, 09 Apr 2025 02:18:12 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed7ecd5d4a2a5154634b3703d219a51f19c2177b91f7d951cb5cb4a224c47f1`  
		Last Modified: Wed, 09 Apr 2025 02:18:12 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b92ca15f9a89c22756717858d4a1b19775febe7fa29ed48666b1e2791b4d75`  
		Last Modified: Wed, 09 Apr 2025 02:18:12 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4678982d980d4d13502ad484db7f18ad4d16f900777a126d0fb914eee58f69`  
		Last Modified: Wed, 09 Apr 2025 02:18:12 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7146b143f4a9e84ae822c387f9e22428966b9ba6131e0a8094cca92305e45967`  
		Last Modified: Wed, 09 Apr 2025 02:18:11 GMT  
		Size: 76.3 KB (76280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3179be0cc264cb26c339e78aabd0eca1838254df08dee4f285db8f671b378dfd`  
		Last Modified: Wed, 09 Apr 2025 02:18:11 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2a734a1b9bd143998fc4b584730d1d0fd728ca8beda564f1700b66a3f90f04`  
		Last Modified: Wed, 09 Apr 2025 02:18:21 GMT  
		Size: 187.2 MB (187235436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b331e0c7befaf81019a2a02861ec6fdfb844f9e56ad5a56b88cc38d20d4303e`  
		Last Modified: Wed, 09 Apr 2025 02:18:11 GMT  
		Size: 124.0 KB (124036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff00bc7557a764a7cf0b34dc4bbc40fed4a7f33ecd09e1d102bb704c511f7e14`  
		Last Modified: Wed, 09 Apr 2025 02:18:11 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
