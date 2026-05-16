## `openjdk:27-ea-22-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:38efe10ca18392786d273a2e9c5ec6a0cdcdefa8e7a0071dc45b08a6f8fa3b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-22-jdk-nanoserver` - windows version 10.0.26100.32860; amd64

```console
$ docker pull openjdk@sha256:b6bbb7f160577d102342d9f386f438bcb9a1663299763590b3626ac3330c057f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.8 MB (424846154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fa7b27160e70d081a5b8473b0df7ed12499ba0d54579bec7787ede87fde6b6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Fri, 15 May 2026 21:41:07 GMT
SHELL [cmd /s /c]
# Fri, 15 May 2026 21:41:07 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 15 May 2026 21:41:07 GMT
USER ContainerAdministrator
# Fri, 15 May 2026 21:41:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 15 May 2026 21:41:14 GMT
USER ContainerUser
# Fri, 15 May 2026 21:41:14 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 21:41:56 GMT
COPY dir:26616ed4ec7ce92992021f6a1b897f31b1ceeabfdf08d8708ce4a218012d3963 in C:\openjdk-27 
# Fri, 15 May 2026 21:42:02 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 15 May 2026 21:42:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d248295791e535497d24d835947bdecc3e09c15f8917f0d8a3d8ee3e4ccf2e48`  
		Last Modified: Fri, 15 May 2026 21:42:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72082aab6d2ae5155f9111e90b84f35afebc187bfb618a185bdba12ee74d2a2`  
		Last Modified: Fri, 15 May 2026 21:42:08 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5cf8203701a03b5249d5c162e3b9caafc2aab9f87b5e167b83823c7cef54a6`  
		Last Modified: Fri, 15 May 2026 21:42:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a72b5776510f0a47691706468b90399298a367cf4a2a6b89105d3b256a7030a`  
		Last Modified: Fri, 15 May 2026 21:42:08 GMT  
		Size: 69.4 KB (69408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d386026fca68444244497d79b1625f27025171ebedf28fa542c5d49872d939`  
		Last Modified: Fri, 15 May 2026 21:42:06 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5002b4d6dbf2d5ea73d2dc002211e5cf1054957eb0820481c44e6c36e4659180`  
		Last Modified: Fri, 15 May 2026 21:42:06 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6218c9f95e4fbbb94be9a1a742b8435bc196ee78fc01f1baccf6b30851332c2d`  
		Last Modified: Fri, 15 May 2026 21:42:20 GMT  
		Size: 224.9 MB (224928564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7130e3e1082c0e2070b9cfd35feeedfe756bceed9802017bb8baecc2c43f8e1`  
		Last Modified: Fri, 15 May 2026 21:42:06 GMT  
		Size: 102.9 KB (102940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5550b64995b57edb5400ee5fa6d40eb665b72ba5109a44b1a5a4ce0fdc01c5`  
		Last Modified: Fri, 15 May 2026 21:42:06 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-22-jdk-nanoserver` - windows version 10.0.20348.5139; amd64

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
