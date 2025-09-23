## `openjdk:26-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:ef63f0b2505df260c7e0ce149870d8f0b9debf4a097fc4054b99688eb64bcb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:a7775db104752b3ddc47e43de612a8b899d7100610eb1a76ef8db4d3b077067e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341837983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d2d08fd55723552714208a964692dc02b808fb1e42f345a7a5a70ffea16844`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Mon, 22 Sep 2025 23:14:43 GMT
SHELL [cmd /s /c]
# Mon, 22 Sep 2025 23:14:44 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 22 Sep 2025 23:14:45 GMT
USER ContainerAdministrator
# Mon, 22 Sep 2025 23:14:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 22 Sep 2025 23:14:53 GMT
USER ContainerUser
# Mon, 22 Sep 2025 23:14:54 GMT
ENV JAVA_VERSION=26-ea+16
# Mon, 22 Sep 2025 23:15:35 GMT
COPY dir:426c5eff4433821d86546e9933d9e51369c584ab771442942f2429c3418779a2 in C:\openjdk-26 
# Mon, 22 Sep 2025 23:15:42 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 22 Sep 2025 23:15:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431fb9503389315a2b945a76ebf638702405b8ffd6489a6baeaa24ac36b092f7`  
		Last Modified: Mon, 22 Sep 2025 23:16:10 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb08042aa117f148bb267b1e6a998c6259fef67a15678e6c011a04563021662b`  
		Last Modified: Mon, 22 Sep 2025 23:16:10 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad40894bc97fd3b1452fed478d0a29fc2f648113b85c981fe22bb2fd76acc49e`  
		Last Modified: Mon, 22 Sep 2025 23:16:10 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da44c5adc244703c5fc739b41a0a0ae8ea5284ba1c16254958da7c5576e4ac88`  
		Last Modified: Mon, 22 Sep 2025 23:16:10 GMT  
		Size: 71.6 KB (71632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f8eb2632be96700850db69483b09d8c5dd6a5309d463b8e3286db57bc3410d`  
		Last Modified: Mon, 22 Sep 2025 23:16:10 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1a80ae3d9cfee7380158286fea86a7442f9d30b2a3e3492aa2e7195eebc2d`  
		Last Modified: Mon, 22 Sep 2025 23:16:10 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa18ae7d5ccd35f827cf58f8c59259b23fb0e1a6d0f3ac866d61879f5f6ce16`  
		Last Modified: Tue, 23 Sep 2025 00:24:11 GMT  
		Size: 218.9 MB (218905438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb7d79b4cc3105bbab0dad4e8be77c3055f140551ddb82d4b51f0bf805b2354`  
		Last Modified: Mon, 22 Sep 2025 23:16:10 GMT  
		Size: 134.6 KB (134592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bf5408866e7218f48fd933b0af67a1715ad56a7cac4e8f5db5ca5b91eb05bc`  
		Last Modified: Mon, 22 Sep 2025 23:16:10 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
