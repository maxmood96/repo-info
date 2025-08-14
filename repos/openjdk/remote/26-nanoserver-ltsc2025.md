## `openjdk:26-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:1b6c1494e951c59168184c02d244b15497f30db3850a56ea2f9a92d7c76e1171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `openjdk:26-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

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
