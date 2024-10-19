## `openjdk:24-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:15bd1c354e75e0d54e27361f48522bf0430e47e490a6fb2c5826dd588a96fb77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-jdk-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:df4803ef553cd7a8ef25503c7d5245b084d4b5a8038e5402e8a6eb7defb31802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 MB (367953387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301a9a5375eddb811012850636cac4ad43df6b55592aa42834fe6ca69398d260`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 19 Oct 2024 02:07:45 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:07:46 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 19 Oct 2024 02:07:46 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:07:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 19 Oct 2024 02:07:55 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:07:55 GMT
ENV JAVA_VERSION=24-ea+20
# Sat, 19 Oct 2024 02:08:05 GMT
COPY dir:a71b07dc83da64145e14b1d79f8079fcefb25f442a78d8409aeafff83e71116c in C:\openjdk-24 
# Sat, 19 Oct 2024 02:08:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 19 Oct 2024 02:08:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231773452a79cce946e1b8c22242231d4cc69e29eef8546144ac76899a3c6a22`  
		Last Modified: Sat, 19 Oct 2024 02:08:16 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda618d1d653af4c1fa9e00224b6cf4466e2637a90e505656130ea548d5153cd`  
		Last Modified: Sat, 19 Oct 2024 02:08:16 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649c48b7849013050bc9912fab49f315d5458d10c6c7717e8e544d437bf4e69d`  
		Last Modified: Sat, 19 Oct 2024 02:08:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3839b55e0b10c4a9be127d4895f742f6dc2b0f1a3a27d041ca5a4ca736469e8`  
		Last Modified: Sat, 19 Oct 2024 02:08:16 GMT  
		Size: 67.8 KB (67757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf14c55b40848d47a7f2a193676ac23f82a72be901fec5ec87d3f2b2f3de26`  
		Last Modified: Sat, 19 Oct 2024 02:08:15 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0f3c1bba706f705682da0abe4d8f218829d812cb94cb95cf130249d607ad2a`  
		Last Modified: Sat, 19 Oct 2024 02:08:15 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bac23dc7a90522c89db141d21fbcca2848f6561522ba618db473853e702d39`  
		Last Modified: Sat, 19 Oct 2024 02:08:25 GMT  
		Size: 208.2 MB (208197531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194935642eb8006ce92b62b29dd975a76876d1ae1d9320e93e711e01de46a409`  
		Last Modified: Sat, 19 Oct 2024 02:08:15 GMT  
		Size: 4.6 MB (4588247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398af93f10708c07411509b801442ddf73bd1e1088843500fdbce0cf0590686d`  
		Last Modified: Sat, 19 Oct 2024 02:08:15 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
