## `openjdk:25-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:19dad1cd60ff13905c898ea504dfab59270d8cd710bed3ac30a3b891cd9ae5ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:25-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:f06e0f86a8378d6bf49a9022f686830f5a46b0a00a7a66df7f30d609ec007869
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.8 MB (406771820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e37996a069e67865dc7ff82c80cd2a05f0f4290f83f272394d8a2ed092085f8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Sat, 15 Feb 2025 00:36:54 GMT
SHELL [cmd /s /c]
# Sat, 15 Feb 2025 00:36:55 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 15 Feb 2025 00:36:55 GMT
USER ContainerAdministrator
# Sat, 15 Feb 2025 00:36:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 15 Feb 2025 00:36:58 GMT
USER ContainerUser
# Sat, 15 Feb 2025 00:36:59 GMT
ENV JAVA_VERSION=25-ea+10
# Sat, 15 Feb 2025 00:37:06 GMT
COPY dir:9943a6a8676ba9b798cfd35aa38f439443e45eb2bb7f1445736d316c89a33808 in C:\openjdk-25 
# Sat, 15 Feb 2025 00:37:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 15 Feb 2025 00:37:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed9eea6d5b0834cea604480c495d2e4f8db63689f04d94ca38d4e0c87581302`  
		Last Modified: Sat, 15 Feb 2025 00:37:19 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66281eb358fa0a0ff14be3d9bb2492c74757536f34c0d580a6c10b90808c49a6`  
		Last Modified: Sat, 15 Feb 2025 00:37:19 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cc0900c2682a6af795013e6de84a92b8aa691b0e44e6bbb00dd91a884e6598`  
		Last Modified: Sat, 15 Feb 2025 00:37:19 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262c4202d3e4d2dd20a5ab2b6f615285d2e210577720fde6dc230ee8aa21c679`  
		Last Modified: Sat, 15 Feb 2025 00:37:19 GMT  
		Size: 75.7 KB (75662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9e32519e19ee14c4aec0f0fc3ae6f98db7bfdb2732a3dad61dbc35002063e0`  
		Last Modified: Sat, 15 Feb 2025 00:37:17 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5586b86200c4d34088e43fb14cfdf4792a64114c8a09b530293457cb23586adf`  
		Last Modified: Sat, 15 Feb 2025 00:37:17 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038c9c7d18ff58a9f6c506cb431ee38dd67f791a018ef1831c6e0b00430e1d99`  
		Last Modified: Sat, 15 Feb 2025 00:37:28 GMT  
		Size: 207.5 MB (207542520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10347d89d688de355a6e7d5fed0fffe6b9c450dc3b1f26ce1a5d87d17db57f1a`  
		Last Modified: Sat, 15 Feb 2025 00:37:17 GMT  
		Size: 93.1 KB (93105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfa43d7af484d75f2fc115614cc435c4d070b7a4cc05040bff6f1f84e972ba6`  
		Last Modified: Sat, 15 Feb 2025 00:37:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
