## `openjdk:25-ea-25-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:a85f810b48768e9539a8aedde729360b4da0eacbf612aa355ead7b243192d50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `openjdk:25-ea-25-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:5d8a27cc131997f924fe8600af9d74b8d71ce4a01cc78ead2727cd12e10cb24c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.7 MB (409720052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09688d605efdfe0fd3c7c28c43dc37a12fc4cc6310b56436e1f227103c0e8055`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Fri, 30 May 2025 18:03:06 GMT
SHELL [cmd /s /c]
# Fri, 30 May 2025 18:03:08 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 30 May 2025 18:03:09 GMT
USER ContainerAdministrator
# Fri, 30 May 2025 18:03:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 30 May 2025 18:03:15 GMT
USER ContainerUser
# Fri, 30 May 2025 18:03:16 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 18:03:26 GMT
COPY dir:bd2747e79afdad77e7098a4e268355ea8695f52ce1251320a131b555b1a0c1b4 in C:\openjdk-25 
# Fri, 30 May 2025 18:03:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 30 May 2025 18:03:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323094c275efe01fca7ffff0b61c1449ac7e2b9f4b1c8eef5dc35cc9fd636c4f`  
		Last Modified: Tue, 03 Jun 2025 17:19:43 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656abf191e3ace4ff066c5ee9a9e965f9cbcdf249f05a4ef8f03f969523c6a6f`  
		Last Modified: Tue, 03 Jun 2025 17:19:43 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4aa94071760898b6dffbeb6d43dcdbdaa98be19654a4c3225a8287dd567b549`  
		Last Modified: Tue, 03 Jun 2025 17:19:44 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4382dcd655701a34d1b16968536aa0f05f27c4a66bc54fe2157f9c928435fd`  
		Last Modified: Tue, 03 Jun 2025 17:19:44 GMT  
		Size: 77.1 KB (77087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7d636ff8c676a81ca1722eead009869d60378b40917cd448ae70cf1276d001`  
		Last Modified: Tue, 03 Jun 2025 17:19:45 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8da085131c5cff8eb626f955068174b7b6ceb834de81851005345069d17264d`  
		Last Modified: Tue, 03 Jun 2025 17:19:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159487d6bfffecc5589698eaae94cd1eb6dc2fb7c9c376c33fa615c38bb7a5d7`  
		Last Modified: Tue, 03 Jun 2025 17:20:00 GMT  
		Size: 218.1 MB (218117715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3926f146141a182889cfabc70adae0b44e53b384538b2dc3101e7dad701ee19e`  
		Last Modified: Tue, 03 Jun 2025 17:19:47 GMT  
		Size: 106.9 KB (106927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f103593afc840722d81523f96ec6a498fdae44c6dffef5301a15a0e03977de8`  
		Last Modified: Tue, 03 Jun 2025 17:19:48 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
