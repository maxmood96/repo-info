## `openjdk:26-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:0953009c7c37d0994fba167247194885826d30a2797ba142f69d5f47218294b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-jdk-nanoserver` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:6b8239e5c1be1e40ad626f10d1092498c8b24acb5e3f6b352b852a97417facc1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.3 MB (412251889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001ee320803fdbbcc64fa19c2ec9ce5a7627e9a8f09064263cc0f7987c7b414f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:50:28 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:28 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 12 Aug 2025 20:50:28 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 12 Aug 2025 20:50:30 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:31 GMT
ENV JAVA_VERSION=26-ea+10
# Tue, 12 Aug 2025 20:50:37 GMT
COPY dir:276e3287dbd797dcc8c487ef64a14aeb0bc052e24933e6ffdff79aeb51065696 in C:\openjdk-26 
# Tue, 12 Aug 2025 20:50:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 12 Aug 2025 20:50:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02ded881e7a34a560da4bcf62c3f2bcc3a5854400eb93130bf5185d59249c98`  
		Last Modified: Tue, 12 Aug 2025 20:51:42 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51c752b81ff39c8c2ac5f0c26d5323ed941e0acf0d66b97cd4a078a634c9284`  
		Last Modified: Tue, 12 Aug 2025 20:51:42 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df360185dc8f0d74caea1f8552146f3bb5f9b77e60e9a6ddd092798c2ea7cd3e`  
		Last Modified: Tue, 12 Aug 2025 20:51:42 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1004891f59e42aef0c37992160bc73017cdfc1f9f57a943942d34575098415`  
		Last Modified: Tue, 12 Aug 2025 20:51:40 GMT  
		Size: 75.5 KB (75467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1820fba543a240341d84012768d468a71a2a09a2af1182028d752935d66b74e`  
		Last Modified: Tue, 12 Aug 2025 20:51:38 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc805f69485b92ed22bc661f9bd70107fe55bec0f1421b7356d3cab4f9f8caf`  
		Last Modified: Tue, 12 Aug 2025 20:51:38 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b280286307c2d0a5bc36a22b5d63990e41bd4bdbfc2cea4ca6eb9cd54f033477`  
		Last Modified: Tue, 12 Aug 2025 21:25:40 GMT  
		Size: 218.6 MB (218587321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce7324cbde279f3676438de1fc888d59f03b70542373e8e750b68c4bba032d`  
		Last Modified: Tue, 12 Aug 2025 20:51:40 GMT  
		Size: 113.2 KB (113217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3d833a00e1d71de696d858f0e8faeaac654c82101aa41084b7e32dc40a9d1f`  
		Last Modified: Tue, 12 Aug 2025 20:51:40 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:cede5881779d318cea909692d93b9edc3157bdd8063af3e734be73d0be4e0361
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341430213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cd89bba1720eabd39c9ac1025b0ccd2ec3f542f2e7ba2049f38c6969e8a84e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:49:56 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:49:58 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 12 Aug 2025 20:49:59 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 12 Aug 2025 20:50:03 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:04 GMT
ENV JAVA_VERSION=26-ea+10
# Tue, 12 Aug 2025 20:50:13 GMT
COPY dir:276e3287dbd797dcc8c487ef64a14aeb0bc052e24933e6ffdff79aeb51065696 in C:\openjdk-26 
# Tue, 12 Aug 2025 20:50:19 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 12 Aug 2025 20:50:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46e64b9790e92043fe38a4d4c4b13bad9b6efb5a722ba18958c7c8d23ff27e`  
		Last Modified: Tue, 12 Aug 2025 20:51:09 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e1c089df487ff08c23c589cf90dceb98f29096e3bb6a5e5ebf324d57a046a3`  
		Last Modified: Tue, 12 Aug 2025 20:51:09 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401fbf42b2526cbb4319fbc0a1baac9affbd2ca353a0ac6387f5db3a4880f782`  
		Last Modified: Tue, 12 Aug 2025 21:25:24 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7b69ae52bffd81c0b1fb3997ecda718984a472ef25ab57ade15a25941a7815`  
		Last Modified: Tue, 12 Aug 2025 21:25:24 GMT  
		Size: 78.4 KB (78366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4cc3090ca9a2f2885a9a52277448053bb8885a032f1f23402f33ca8477d7fe`  
		Last Modified: Tue, 12 Aug 2025 20:51:12 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc85afcd816abfadd9e37557f4475486e9c3d9f37899e7b3df483f4666546b27`  
		Last Modified: Tue, 12 Aug 2025 20:51:12 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53ca6693ca1185959aa33c352f91b832c544e7d8a1b8655b4793bfe93eb696`  
		Last Modified: Tue, 12 Aug 2025 21:25:36 GMT  
		Size: 218.6 MB (218587180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9f2109f7e5cc7d9b2748783a502dec42770ffb8afea0fc29653ab6b0ba9a0b`  
		Last Modified: Tue, 12 Aug 2025 20:51:12 GMT  
		Size: 98.2 KB (98150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e9428cd066abf3b8fc0f064e1860032b7d29f25ce194f40c4923ec91ecfcb8`  
		Last Modified: Tue, 12 Aug 2025 20:51:12 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
