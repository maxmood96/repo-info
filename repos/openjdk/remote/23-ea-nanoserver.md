## `openjdk:23-ea-nanoserver`

```console
$ docker pull openjdk@sha256:479c2cb2d65c53a1aea84b1358040a4a05f8b46a3d25c3333dc88ceeb66baa20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `openjdk:23-ea-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull openjdk@sha256:b5531e0517bc9d39aedc7cae3a1970ac45c794bec9b39932a4c2a78ab90a3250
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.3 MB (366264560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed9862146d36a3407927147ca875d4fd028168038b4d5de8d42747f0f70d724`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Mon, 10 Jun 2024 23:44:15 GMT
SHELL [cmd /s /c]
# Mon, 10 Jun 2024 23:44:17 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 10 Jun 2024 23:44:18 GMT
USER ContainerAdministrator
# Mon, 10 Jun 2024 23:44:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 10 Jun 2024 23:44:23 GMT
USER ContainerUser
# Mon, 10 Jun 2024 23:44:23 GMT
ENV JAVA_VERSION=23-ea+26
# Mon, 10 Jun 2024 23:44:32 GMT
COPY dir:40a82c570517dedd498b0b8d242aa1177d065a56837a01711f48d67cb3613213 in C:\openjdk-23 
# Mon, 10 Jun 2024 23:44:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 10 Jun 2024 23:44:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f26da63603ad00d80c1fdf94ad436dbf1a443f33c0fb701f815e5fb90d2e1f`  
		Last Modified: Mon, 10 Jun 2024 23:44:49 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090ed914002d531b915c5d732486028a08004b6b74fae28fae9c5237b32c6a07`  
		Last Modified: Mon, 10 Jun 2024 23:44:48 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddbfcf08d8dd34a43bcf1d7ceff5520f50bd919dbc1427107f03f6b03024bd3`  
		Last Modified: Mon, 10 Jun 2024 23:44:48 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdef74f7ff5c07b25b764d882eb4e6d6bf0b9bbfac4623e660cf8dbc248f4f23`  
		Last Modified: Mon, 10 Jun 2024 23:44:48 GMT  
		Size: 68.4 KB (68404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933cf3353265ce7d342c9673480b15e224260e34db26a0897b2eb3b70936a138`  
		Last Modified: Mon, 10 Jun 2024 23:44:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd34855a160084fcf74303a5e8a6c6d24894503e267e668d058d0f83aee0803`  
		Last Modified: Mon, 10 Jun 2024 23:44:46 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fad249b56400924b0ffd2e24b23e99a4126abb5a08c9dfac2c5cb26708157b1`  
		Last Modified: Mon, 10 Jun 2024 23:44:57 GMT  
		Size: 206.0 MB (206041034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fc363fcab3955853dd58e86dde13c4a3e36b546608e2a22a9ee46243a46cd3`  
		Last Modified: Mon, 10 Jun 2024 23:44:47 GMT  
		Size: 5.2 MB (5207489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecab7eab7febbc374302fdfc709a15e167a17ce167bce7486037869759e06882`  
		Last Modified: Mon, 10 Jun 2024 23:44:46 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
