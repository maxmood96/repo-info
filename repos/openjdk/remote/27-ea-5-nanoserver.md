## `openjdk:27-ea-5-nanoserver`

```console
$ docker pull openjdk@sha256:415874ad4a4e9bfbfe99d3799b918b1a7abdfbec4c02aaa2d19a63696b76a4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-5-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:b36148e82ae040dd64d4e75da15ebaa08d5ad9ef61e751231eca8c11785f1751
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.3 MB (423344166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fc97a540238f87fe110a7c2ded41d3eb9fe32fdf9c09ceb46095bacdacdb61`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 20 Jan 2026 19:10:15 GMT
SHELL [cmd /s /c]
# Tue, 20 Jan 2026 19:10:16 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 20 Jan 2026 19:10:16 GMT
USER ContainerAdministrator
# Tue, 20 Jan 2026 19:10:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 20 Jan 2026 19:10:23 GMT
USER ContainerUser
# Tue, 20 Jan 2026 19:10:24 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 19:11:18 GMT
COPY dir:2351caaa563662896c889f1c7ad17c3ab77559d0da2169277ad297474751eb8c in C:\openjdk-27 
# Tue, 20 Jan 2026 19:11:26 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 20 Jan 2026 19:11:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:56 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bb79b3f25815a4d814fa8197fc1d6952e6573864667142cd18bd7fd7d9c23c`  
		Last Modified: Tue, 20 Jan 2026 21:12:27 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6041a31509244388cc96d4b36732643d4fd474cad9778debee3c97578469b76`  
		Last Modified: Tue, 20 Jan 2026 19:12:00 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a16a10cb61455a026444501c2393871e175450e8161d710a1ec53762dc90fb9`  
		Last Modified: Tue, 20 Jan 2026 19:12:00 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d062c8c4fb694f1707a61f50c8597ebb4470661b7d663b70ad143ca4c2f51269`  
		Last Modified: Tue, 20 Jan 2026 19:12:00 GMT  
		Size: 72.4 KB (72427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dd03f409914f0d2fd15f21a60a3ce3f2812384c399dbba2d8a0c3af4bb5311`  
		Last Modified: Tue, 20 Jan 2026 19:11:35 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b8020253c57c12a8001106d743dd359673de2e44e0d1f60fdf81dfd182a31`  
		Last Modified: Tue, 20 Jan 2026 19:12:01 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce9edc95096a382dbb63e6fe197ee07b0566817f1404edc6beba29ddd4b6695`  
		Last Modified: Tue, 20 Jan 2026 19:36:43 GMT  
		Size: 224.1 MB (224064770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c2e35e6dae16540723f3b5900e94bff822174916beded5f42ce4baef336ba`  
		Last Modified: Tue, 20 Jan 2026 19:11:35 GMT  
		Size: 124.0 KB (123989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6b902aded73807fc04779e2a0a1f16a951711b1f99b610fdc6b0fdd128e50f`  
		Last Modified: Tue, 20 Jan 2026 19:11:35 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-5-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:567640ea37a1086348fc8773600142b5df59cdd988e597cb97668351d1b07f82
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350947324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2023f2f0416737542458591be0ad9a3449d6d3c32bbc9b6338edb5a5e4994e70`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 20 Jan 2026 19:10:17 GMT
SHELL [cmd /s /c]
# Tue, 20 Jan 2026 19:10:18 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 20 Jan 2026 19:10:19 GMT
USER ContainerAdministrator
# Tue, 20 Jan 2026 19:10:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 20 Jan 2026 19:10:27 GMT
USER ContainerUser
# Tue, 20 Jan 2026 19:10:27 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 19:11:42 GMT
COPY dir:2351caaa563662896c889f1c7ad17c3ab77559d0da2169277ad297474751eb8c in C:\openjdk-27 
# Tue, 20 Jan 2026 19:11:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 20 Jan 2026 19:11:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:12:21 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0a2970dbd57fe2611f8d055a2a986babe557bf17d3a1826ec73a7a74b1256`  
		Last Modified: Tue, 20 Jan 2026 19:11:54 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceee124e21ec0baec35681f7b0ff4d4db13430742ed7c3fb517e24fe1d2dfaf4`  
		Last Modified: Tue, 20 Jan 2026 19:12:17 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d569e82d18e6f3b3220fb9cf8e6aefd2870d9b14c408ade512491fc753c013c`  
		Last Modified: Tue, 20 Jan 2026 19:12:17 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d05e888cd70f911322997bfdc82d2571c2dd0029c997cef6606b149012bc286`  
		Last Modified: Tue, 20 Jan 2026 19:12:14 GMT  
		Size: 72.0 KB (71992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5b7430fd074222076fc93e7efe53160f1b2c964d62be5280646d6809d30493`  
		Last Modified: Tue, 20 Jan 2026 19:11:53 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c3c010797e2d0ef9aa380caa23e50fbbe98bb948609e29e088cce2994a254c`  
		Last Modified: Tue, 20 Jan 2026 21:14:25 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73d70450b1b655bf798c34647e06aa651460d5f6fb3bfe842cfc1439848c4f1`  
		Last Modified: Tue, 20 Jan 2026 19:12:09 GMT  
		Size: 224.1 MB (224064674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effb8c50ea198944f34e90748e3486e77c386e81179c402f04478c6fddd9f35f`  
		Last Modified: Tue, 20 Jan 2026 19:12:14 GMT  
		Size: 107.5 KB (107485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300ae2ac5098565d7965b9b00ce61e5e7364605d9ee7a557da22bcb877b91108`  
		Last Modified: Tue, 20 Jan 2026 19:12:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
