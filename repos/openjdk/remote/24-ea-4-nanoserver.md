## `openjdk:24-ea-4-nanoserver`

```console
$ docker pull openjdk@sha256:cc9da749a8a56e6c327905241fe565711daf3f43f02be3161971ba85d28ea225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-ea-4-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:592ecd6ab759217b08bdab28cbe45f70b6627abff0b3c89de2deb99d7279905a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.4 MB (366384540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d747d7e21451e09748a012100a03b870f7643bd67c8612f1d5211b3dc545d2a0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Tue, 02 Jul 2024 03:13:42 GMT
SHELL [cmd /s /c]
# Tue, 02 Jul 2024 03:13:43 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 02 Jul 2024 03:13:44 GMT
USER ContainerAdministrator
# Tue, 02 Jul 2024 03:13:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 02 Jul 2024 03:13:52 GMT
USER ContainerUser
# Tue, 02 Jul 2024 03:13:53 GMT
ENV JAVA_VERSION=24-ea+4
# Tue, 02 Jul 2024 03:14:00 GMT
COPY dir:8c6411dffb872fd52493a71ade2bed60c61534f62d9335544c448b4f7a7c4309 in C:\openjdk-24 
# Tue, 02 Jul 2024 03:14:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 02 Jul 2024 03:14:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43095778aa5043848a070d7238b7ea92269b8224c118114f0e033aa3c3773be3`  
		Last Modified: Tue, 02 Jul 2024 03:14:19 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475dd74259826c9c4cc0f8873800d075a9d33d5930534c2fad9fc802c0a12905`  
		Last Modified: Tue, 02 Jul 2024 03:14:18 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3e73baeb6e447480c7243cb2be3765e921f41b986033cb1131cd34042839d4`  
		Last Modified: Tue, 02 Jul 2024 03:14:18 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478719caeffcf2bb353ace8538d8aedb877da8c3abfa4e9603bc73ef166b0272`  
		Last Modified: Tue, 02 Jul 2024 03:14:18 GMT  
		Size: 69.4 KB (69373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d15744c2010aa902052ab47a2af8c6f30b378b933de40746678a37fd5db7974`  
		Last Modified: Tue, 02 Jul 2024 03:14:16 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2634ab8da1b315b54bc54c112566cc586c47bb4d70ea90ebd8532b9c248adfd`  
		Last Modified: Tue, 02 Jul 2024 03:14:16 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e642a78eaadddede48e9077250ab8106058adc2a04a331b958556c679ed510e4`  
		Last Modified: Tue, 02 Jul 2024 03:14:26 GMT  
		Size: 206.1 MB (206122352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e524858330a8102e41299caf580b439f3029090c234017443826a3f82ffea451`  
		Last Modified: Tue, 02 Jul 2024 03:14:17 GMT  
		Size: 5.2 MB (5153394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9aadc3e8a1898d803f478b4de952623757786835710490df86427a7df7239f0`  
		Last Modified: Tue, 02 Jul 2024 03:14:15 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
