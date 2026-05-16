## `openjdk:27-ea-22-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:2630f147f5b946bbcbd70b3630d8c6734854917456e999093b546a9f384de97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-22-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:400889f864d06c5a60e2d994067c11bbcf246b8c966aeee5bb3c35c775b36dba
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352161951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc28f0d4af34301b6104458937a9168f3528f164f1fbafe6a8f6ef2b8b5d1900`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Fri, 15 May 2026 21:25:56 GMT
SHELL [cmd /s /c]
# Fri, 15 May 2026 21:29:00 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 15 May 2026 21:29:00 GMT
USER ContainerAdministrator
# Fri, 15 May 2026 21:29:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 15 May 2026 21:29:02 GMT
USER ContainerUser
# Fri, 15 May 2026 21:29:03 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 21:29:54 GMT
COPY dir:26616ed4ec7ce92992021f6a1b897f31b1ceeabfdf08d8708ce4a218012d3963 in C:\openjdk-27 
# Fri, 15 May 2026 21:29:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 15 May 2026 21:30:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb8e31ecd6facd70d76050945945bacc13c73575e37bcfbdacaa45ee57464c7`  
		Last Modified: Fri, 15 May 2026 21:27:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03842512e0146e8ed76466710b1fdffb1891f0f3f5531236baad1b70bc7c3d0a`  
		Last Modified: Fri, 15 May 2026 21:30:06 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec0d3011956431eb0234a4f4bc4554e7531ffa12408ff472ea4662536deb32e`  
		Last Modified: Fri, 15 May 2026 21:30:06 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e776be16c8a77c3303fe32b5503110719d9c8c7e6da58239f72cc7e74423072`  
		Last Modified: Fri, 15 May 2026 21:30:06 GMT  
		Size: 76.9 KB (76922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a339f0aecc9922a30a53112ba82abc63062fa42d831f45f33be2745c879d1c`  
		Last Modified: Fri, 15 May 2026 21:30:04 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1771f23a4c74eed53d5b6917b4a4332fead27146aa79d06c5fc2ddd06957dc61`  
		Last Modified: Fri, 15 May 2026 21:30:04 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2059ddaf5308aba96b1087a619ce67659a047fc3452081ccfe1eeae308a658`  
		Last Modified: Fri, 15 May 2026 21:30:19 GMT  
		Size: 224.9 MB (224928724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948375c5c72d447ef1a6432e876a473ce4de98585f9761d0b90b25b7465dfb7c`  
		Last Modified: Fri, 15 May 2026 21:30:04 GMT  
		Size: 111.1 KB (111079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c8f83ef094e69764389aa729e38b09396e94e7b51940117c649aa39e8cad6b`  
		Last Modified: Fri, 15 May 2026 21:30:04 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
