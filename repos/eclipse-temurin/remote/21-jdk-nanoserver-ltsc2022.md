## `eclipse-temurin:21-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:94b122ec132f2c72222466499087cae755dd19d8d0dbe11a6e0c0bde34cb264b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:c3b42259866c8c2fa321bb23b954433822f6a25bd4d803cb8770560f051f77f2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324206480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1cccaafad55d20b8d51d5524e229fa6abd0d29bf8904fc42d323b4694ecfb9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:18:26 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:18:27 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 18 Apr 2025 04:18:28 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 18 Apr 2025 04:18:29 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:18:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:18:32 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:18:40 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Fri, 18 Apr 2025 04:18:45 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:18:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f056659c7ba83e0261150d3b401324033b4d4182600dc7514018be52c80ed5`  
		Last Modified: Fri, 18 Apr 2025 04:18:52 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fb1d474365ca1fd790494efed929da78d3546c2238a359f80322fe3d204f36`  
		Last Modified: Fri, 18 Apr 2025 04:18:51 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436ef6621addb9d04e2ee6d8fc7052b2ab3777795171514abf5aca7729d74fae`  
		Last Modified: Fri, 18 Apr 2025 04:18:51 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ad100f505917ff762884972ac65a58fed8ba8e52c9ea7ebb972aef54ffa338`  
		Last Modified: Fri, 18 Apr 2025 04:18:51 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffef8d88bc09e650e1fc805e5a5766fbaa025c6f7ab9c601198b44536a756976`  
		Last Modified: Fri, 18 Apr 2025 04:18:49 GMT  
		Size: 78.2 KB (78188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137d464b6d2a96ecb9984eb7746b459af1d6f5ff011181fbfb51759fd0e19ffc`  
		Last Modified: Fri, 18 Apr 2025 04:18:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f39f2fc56dc3f11c96baf184f259589033498e987854490e6985bc67cd6a387`  
		Last Modified: Fri, 18 Apr 2025 04:19:01 GMT  
		Size: 201.5 MB (201475700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79150e33baf62d6866b2b97f5bd75f7a44219c92b9fafe4c2b4aa54c4a18917a`  
		Last Modified: Fri, 18 Apr 2025 04:18:49 GMT  
		Size: 107.3 KB (107300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1662a8bdc87c3d77ea09543aefcef36b8e05ca50ce8487ff29d7da5deac86f97`  
		Last Modified: Fri, 18 Apr 2025 04:18:49 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
