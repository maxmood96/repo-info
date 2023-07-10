## `openjdk:22-ea-5-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:3519d95187acccffaa675cd4b5da353980ee37558e8c80e813f9dce12f7bc2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `openjdk:22-ea-5-jdk-nanoserver-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull openjdk@sha256:49f5f6ad8c017b7c418b78190336e3fa7d6dc6c98f9fa81949f4ab109f61aa92
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307035362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16327156aeb6bc41332ecfcbe8209723aa6ec5e13d49c9874c6305dd9ab2996`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 21 Jun 2023 07:40:33 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:41:51 GMT
SHELL [cmd /s /c]
# Sat, 24 Jun 2023 03:06:42 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 24 Jun 2023 03:06:43 GMT
USER ContainerAdministrator
# Sat, 24 Jun 2023 03:06:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 24 Jun 2023 03:06:52 GMT
USER ContainerUser
# Mon, 10 Jul 2023 19:22:45 GMT
ENV JAVA_VERSION=22-ea+5
# Mon, 10 Jul 2023 19:23:00 GMT
COPY dir:53a5ac109eca862765e6588e5aa9c5c87ec16f3f74e8b64f135e1fb498e2ad08 in C:\openjdk-22 
# Mon, 10 Jul 2023 19:23:18 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 10 Jul 2023 19:23:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:09087aac643f57e5e24f95fe0a1c8519d0f93dfcf4500263516c0f3874290109`  
		Last Modified: Fri, 23 Jun 2023 02:23:11 GMT  
		Size: 104.4 MB (104400893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09be2e47b3dff420361e93d34eaadedcfd9549c9be5bd77936370792babf874`  
		Last Modified: Sat, 24 Jun 2023 01:24:43 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0720397410cf27e11864dcfc2c9afadd7f7b2969f2bf4a2fd452cc3c6fdb541`  
		Last Modified: Sat, 24 Jun 2023 03:13:44 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2871b71eb8c2564d7544ebac7d7abbfc1ddd2570586a73f216323cab124eedc6`  
		Last Modified: Sat, 24 Jun 2023 03:13:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3912e3db7b6050feb04d0a6219277fd3a5cfb6649ccd27fe845538d11da2ec50`  
		Last Modified: Sat, 24 Jun 2023 03:13:44 GMT  
		Size: 68.8 KB (68757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57de6a9e2121836773f8d9f7079a0c6aab28ae6275690ecdee66946d9a774c6e`  
		Last Modified: Sat, 24 Jun 2023 03:13:42 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da38a0ed0c40f741976d73d7ee64eb39ca8fbc3471f4576819adbcb36a5463f`  
		Last Modified: Mon, 10 Jul 2023 20:18:18 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8719f6657ce85f2da15bd2f0d27ab4d97ba40e80e44e0e11ac65747ac9a4ea0`  
		Last Modified: Mon, 10 Jul 2023 20:18:39 GMT  
		Size: 198.8 MB (198762408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08afb80644de904ee872f0dd1c7b51a0f7911ba090c27417ed7e6a4ea8c23754`  
		Last Modified: Mon, 10 Jul 2023 20:18:19 GMT  
		Size: 3.8 MB (3796665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994ea8cac47dde133c893f1d108360cbdf2fa852ba7b5351a9c00c516083f5a9`  
		Last Modified: Mon, 10 Jul 2023 20:18:18 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
