## `openjdk:27-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:d2a166850b77bcd594539d29687a11829b0a6de3a499928af041d7df7df1c4a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `openjdk:27-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:ebbb22ade2e24bcd26c550eee995d9c056dd40864ac4e1efb3c469585ada9f83
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423964478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbdae8f1b16a302f1ae3a361da023f179903e2e68280d144e76cc3946eef567`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Mon, 23 Mar 2026 19:10:30 GMT
SHELL [cmd /s /c]
# Mon, 23 Mar 2026 19:10:33 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 23 Mar 2026 19:10:33 GMT
USER ContainerAdministrator
# Mon, 23 Mar 2026 19:10:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 23 Mar 2026 19:10:48 GMT
USER ContainerUser
# Mon, 23 Mar 2026 19:10:49 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 19:12:03 GMT
COPY dir:1e03a1eeb0a7b9a5151c618212b4c0b4b3701f1a28f72fad799e2bd29790a005 in C:\openjdk-27 
# Mon, 23 Mar 2026 19:12:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 23 Mar 2026 19:12:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bf29e80d1fd75992fc0fce18981ebd29c465839433846c536be8b695161b62`  
		Last Modified: Mon, 23 Mar 2026 19:12:17 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ac65a694b879efbf5c890f284fa695aa69cdcdaac9e042e5b08a15bf63a62b`  
		Last Modified: Mon, 23 Mar 2026 19:12:17 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da882868ce717a01980946ee73a02dfd548bb7b244f5d0a6b4577f93ad64395c`  
		Last Modified: Mon, 23 Mar 2026 19:12:17 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c4a5811acd879c92bd3389c8343b9a7c467e4dad1077383f98971e0f81a1c3`  
		Last Modified: Mon, 23 Mar 2026 19:12:17 GMT  
		Size: 70.1 KB (70097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cf3993b0be600f74dcd497b8baf1d3e8bec8a8612b4fd58b488ee0989e93b6`  
		Last Modified: Mon, 23 Mar 2026 19:12:15 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01daa444604adb1d61737ceeb1c721a6ab4b9262622cd4d8e0eafef58fe78912`  
		Last Modified: Mon, 23 Mar 2026 19:12:15 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba87180a861100fbbdd2b82be02c9466d3598ac519a850ed27283f65c8f7d24`  
		Last Modified: Mon, 23 Mar 2026 19:12:30 GMT  
		Size: 224.4 MB (224386376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71bb75fe01a5136b372ed91d586db967bff60e82419607f694631c0586ca537`  
		Last Modified: Mon, 23 Mar 2026 19:12:15 GMT  
		Size: 92.3 KB (92287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e367242775bb904a66b560d2abe9d6c79cd083c2119ad61134a7413810daefa2`  
		Last Modified: Mon, 23 Mar 2026 19:12:15 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
