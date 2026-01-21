## `openjdk:27-ea-5-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:d0a3be838718a415ebd4b5f7b7560fde743f8980e6f0c9483c58d8f69db53239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-5-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

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
		Last Modified: Tue, 20 Jan 2026 19:12:15 GMT  
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
		Last Modified: Tue, 20 Jan 2026 19:11:54 GMT  
		Size: 72.0 KB (71992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5b7430fd074222076fc93e7efe53160f1b2c964d62be5280646d6809d30493`  
		Last Modified: Tue, 20 Jan 2026 19:11:53 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c3c010797e2d0ef9aa380caa23e50fbbe98bb948609e29e088cce2994a254c`  
		Last Modified: Tue, 20 Jan 2026 19:11:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73d70450b1b655bf798c34647e06aa651460d5f6fb3bfe842cfc1439848c4f1`  
		Last Modified: Tue, 20 Jan 2026 19:12:09 GMT  
		Size: 224.1 MB (224064674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effb8c50ea198944f34e90748e3486e77c386e81179c402f04478c6fddd9f35f`  
		Last Modified: Tue, 20 Jan 2026 19:11:53 GMT  
		Size: 107.5 KB (107485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300ae2ac5098565d7965b9b00ce61e5e7364605d9ee7a557da22bcb877b91108`  
		Last Modified: Tue, 20 Jan 2026 19:12:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
