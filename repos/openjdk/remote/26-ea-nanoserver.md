## `openjdk:26-ea-nanoserver`

```console
$ docker pull openjdk@sha256:7e883ff0f8aaa8b7f591eb84b1f2a1bfe75f03472b7e41cb7f53b37a5e231358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-nanoserver` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:52b28db21b1a123c0aad05f0fce01fb04b6b865c640a8ba6efeda42bfd7532be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.7 MB (412659295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508c9b32a8fbe6d315470f56d7f452e72180a0ec2a61dc9e4f414716c2321c54`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Mon, 22 Sep 2025 23:12:24 GMT
SHELL [cmd /s /c]
# Mon, 22 Sep 2025 23:12:25 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 22 Sep 2025 23:12:25 GMT
USER ContainerAdministrator
# Mon, 22 Sep 2025 23:12:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 22 Sep 2025 23:12:37 GMT
USER ContainerUser
# Mon, 22 Sep 2025 23:12:37 GMT
ENV JAVA_VERSION=26-ea+16
# Mon, 22 Sep 2025 23:13:28 GMT
COPY dir:426c5eff4433821d86546e9933d9e51369c584ab771442942f2429c3418779a2 in C:\openjdk-26 
# Mon, 22 Sep 2025 23:13:36 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 22 Sep 2025 23:13:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb60081c8a16a463b4f927307d9eea3ac9ded224397c5e9b065b7d761874a5a7`  
		Last Modified: Mon, 22 Sep 2025 23:14:05 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08345df6c61e003c4163af6b5e08e8860516dba5e122db75ca84bfcdacd910`  
		Last Modified: Mon, 22 Sep 2025 23:14:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d2633903dfd6ffefd3bbe7cc24e4d8567f395ea24eb5172ee7ef5c65b885e3`  
		Last Modified: Mon, 22 Sep 2025 23:14:05 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601ef83935eca40d9e51c977f7d1a8b808f61d5b2256c23b0c4cd8bb9919829c`  
		Last Modified: Mon, 22 Sep 2025 23:14:06 GMT  
		Size: 82.7 KB (82728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf0cc6109acb93cc2a135b3e256cbdbc91ddcb646ff5ce43cbb79b09b3e625c`  
		Last Modified: Mon, 22 Sep 2025 23:14:05 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f4531126c8769f223a772d9c63cd0790cbd52e3110cf53772a235f1aa29325`  
		Last Modified: Mon, 22 Sep 2025 23:14:05 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c0a7f7f4ebac06144a8715914512774b17220594e0982b85620d9bbf192309`  
		Last Modified: Tue, 23 Sep 2025 00:24:12 GMT  
		Size: 218.9 MB (218905427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f25ba03b12fd9051e5b864a43f0868c7ea8938fe9c7cb303c418976757ebbc4`  
		Last Modified: Mon, 22 Sep 2025 23:14:06 GMT  
		Size: 113.9 KB (113925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18085c8998b0a893ec43b3c9a99abe0442ea780b4416cd5841b4fb56e080361c`  
		Last Modified: Mon, 22 Sep 2025 23:14:05 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-nanoserver` - windows version 10.0.20348.4171; amd64

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
