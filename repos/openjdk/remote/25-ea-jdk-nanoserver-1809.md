## `openjdk:25-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:150cea23146bff8ff46bdb938bad07a79435b147d6943f82fc6453563cfa7d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `openjdk:25-ea-jdk-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull openjdk@sha256:6ca070e8a8a2e5e19c07321cc5c2377b6fd6b88f593e850f98a9ac7fd66bbd82
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322630738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5b2c8d965f88e6e265808b704b96fb609732ee00c38ba43c0727ea39ad220e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Fri, 23 May 2025 20:11:08 GMT
SHELL [cmd /s /c]
# Fri, 23 May 2025 20:11:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 23 May 2025 20:11:10 GMT
USER ContainerAdministrator
# Fri, 23 May 2025 20:11:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 23 May 2025 20:11:13 GMT
USER ContainerUser
# Fri, 23 May 2025 20:11:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 20:11:21 GMT
COPY dir:d32a1e622c307f990d42f1dfe6052e231c098d4b948c30b3def65fbe5914b454 in C:\openjdk-25 
# Fri, 23 May 2025 20:11:27 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 23 May 2025 20:11:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4a7060407f6f2202ac8da0d62a335eaa0a30c03245c43c623c3175fa13973`  
		Last Modified: Fri, 23 May 2025 20:11:34 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169a032d4a714eab189784eaec4d78c59225be316ecbc1133c076b03eb02eb5d`  
		Last Modified: Fri, 23 May 2025 20:11:33 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256bbf346ee3e469c3d1f400b79de0852273219ec1bc9c66c0891f04954741ba`  
		Last Modified: Fri, 23 May 2025 20:11:33 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cb4a4fc858db0cd44cf3870fb0b45c6420befbafcb3af70a306311d30ae450`  
		Last Modified: Fri, 23 May 2025 20:11:34 GMT  
		Size: 68.8 KB (68810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c93655e3fb8db4251ed8b7fa8d0a44940bd4f4db04c339e66667f5ceccae494`  
		Last Modified: Fri, 23 May 2025 20:11:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264f4235ae8c6b5f855b56c6bf58188c743a0aca5b8c216289b1180f2005dac`  
		Last Modified: Fri, 23 May 2025 20:11:32 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff46d848a1caf39970e1887399504a260fa71b0ae8f9d402b6e7dd13e8648adb`  
		Last Modified: Fri, 23 May 2025 20:11:43 GMT  
		Size: 209.3 MB (209333948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56eb33e20f0982063e73c5464c0765fd44b1fe908af0fb65e6b99ec5acbbcd52`  
		Last Modified: Fri, 23 May 2025 20:11:32 GMT  
		Size: 4.4 MB (4441185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd679f8d4b7d4dba3b31d995803823e6475ceba47d1bdbdbc4e59caa3f01eeb`  
		Last Modified: Fri, 23 May 2025 20:11:32 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
