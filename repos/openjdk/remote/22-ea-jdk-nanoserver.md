## `openjdk:22-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:d28b4f4d0dd387927cf55ccc2450f38d03776d7d0721c0ae8719d25bcab648b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `openjdk:22-ea-jdk-nanoserver` - windows version 10.0.17763.5206; amd64

```console
$ docker pull openjdk@sha256:27f6ad77d5f83d7b06e2b0e8d0d08c8fc05e4341c31bf58b0065566ca9acc83f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305782103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8789b64b92b20da9c873e7918900242da053d59832644cfbd0efa46d9f6e2b39`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Dec 2023 10:54:04 GMT
RUN Apply image 10.0.17763.5206
# Sat, 16 Dec 2023 02:51:48 GMT
SHELL [cmd /s /c]
# Sat, 16 Dec 2023 02:51:49 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 16 Dec 2023 02:51:50 GMT
USER ContainerAdministrator
# Sat, 16 Dec 2023 02:51:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 16 Dec 2023 02:51:52 GMT
USER ContainerUser
# Sat, 16 Dec 2023 02:51:53 GMT
ENV JAVA_VERSION=22-ea+28
# Sat, 16 Dec 2023 02:52:01 GMT
COPY dir:a140597f86a97fd7d707a41d6cb4b8407e32f0f2e9c28260810ecf62af9a4c06 in C:\openjdk-22 
# Sat, 16 Dec 2023 02:52:06 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 16 Dec 2023 02:52:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:424f13a93a185a5defe848e7d270655e05233555f51328c0af24b9e70677d037`  
		Last Modified: Tue, 12 Dec 2023 20:02:40 GMT  
		Size: 104.5 MB (104510104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5277a2193f518d3080010a90b005b01370aa4810940293d4924de995ee179d`  
		Last Modified: Sat, 16 Dec 2023 02:52:13 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececc474386e056f2b8d7dfd68b9176b0477a3b7205e65c3f63b984797647fa2`  
		Last Modified: Sat, 16 Dec 2023 02:52:12 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05f9ca941f50be93d94d8451767eea3f999a26d46d3c30bcee2a96acb596ac0`  
		Last Modified: Sat, 16 Dec 2023 02:52:12 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5d540049a839d718f608e00902dea87b06a8efec3305f8149e3873873e9185`  
		Last Modified: Sat, 16 Dec 2023 02:52:12 GMT  
		Size: 74.6 KB (74560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95257e9ff228ffad21d7951ddcdb911995507e763730276583dc939d47105d4b`  
		Last Modified: Sat, 16 Dec 2023 02:52:10 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8dcf61ecaaad7b1649437f4b9b5b115e825fd5373fb903a283a72b62285341`  
		Last Modified: Sat, 16 Dec 2023 02:52:10 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec1822e9d55f0c214d1f5fff0fbba0234652096ce0dc1fe5788cc85c83ad444`  
		Last Modified: Sat, 16 Dec 2023 02:52:22 GMT  
		Size: 197.3 MB (197326572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64ffb98e9e954b80b3445b3fce794f45ea3daed45fb221723f7e09e8dc0b1b2`  
		Last Modified: Sat, 16 Dec 2023 02:52:11 GMT  
		Size: 3.9 MB (3864164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63650ddf0e779859761472356c3b411393bb128e0124e0337867c5b3b728cf6e`  
		Last Modified: Sat, 16 Dec 2023 02:52:10 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
