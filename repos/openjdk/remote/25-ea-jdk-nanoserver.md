## `openjdk:25-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:14c431cbaadc420ef85099ca67f18c152b8d641ccf6c817ed354287a2bf3a257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.26100.2894; amd64

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

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:5ba8a3998bc6167390d1c608581be8573b0d304eee565d9bc3008c8f563b9a9a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328408088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9a211a58925d97de617ffce4acf7d9414cd2220af6421ee65b548ba753d6e3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Sat, 15 Feb 2025 00:39:39 GMT
SHELL [cmd /s /c]
# Sat, 15 Feb 2025 00:39:40 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 15 Feb 2025 00:39:41 GMT
USER ContainerAdministrator
# Sat, 15 Feb 2025 00:39:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 15 Feb 2025 00:39:44 GMT
USER ContainerUser
# Sat, 15 Feb 2025 00:39:44 GMT
ENV JAVA_VERSION=25-ea+10
# Sat, 15 Feb 2025 00:39:51 GMT
COPY dir:9943a6a8676ba9b798cfd35aa38f439443e45eb2bb7f1445736d316c89a33808 in C:\openjdk-25 
# Sat, 15 Feb 2025 00:39:57 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 15 Feb 2025 00:39:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f38ef4a01d2bc7b03f1c3ea02045fe94989f504c4d8e20e2ea6de9b6f4c282`  
		Last Modified: Sat, 15 Feb 2025 00:40:04 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e900c6c41211b58ea0e7b3d519d67211b3c518897f903e6bfb3c4ca5213f9e5f`  
		Last Modified: Sat, 15 Feb 2025 00:40:04 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da92c08a503e5796b262a6bb532526eab3d5004924618cc6c3ecfdd66110fe`  
		Last Modified: Sat, 15 Feb 2025 00:40:04 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f9f7d0459d13af107e20fcc7a3284c3e9b63522af77e40390e4965997d2fd`  
		Last Modified: Sat, 15 Feb 2025 00:40:04 GMT  
		Size: 76.1 KB (76059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96de596692c52791b0dc053a27fd4a0282808c7305b852c8d356ed7d14283b38`  
		Last Modified: Sat, 15 Feb 2025 00:40:02 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb8f1cad6810334966bd42109f78038d90c17ec23002becce553c57e276f6e`  
		Last Modified: Sat, 15 Feb 2025 00:40:02 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44b0da6b1c93e552c4b92c8f4bbbc3bbb905476fb677a0868cb6fe8365e6620`  
		Last Modified: Sat, 15 Feb 2025 00:40:13 GMT  
		Size: 207.5 MB (207540800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8a36cc5bd22085114918b500546b42c03e830d00d7b4aa9a118e454a6f0c8f`  
		Last Modified: Sat, 15 Feb 2025 00:40:02 GMT  
		Size: 118.4 KB (118401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3dcf8c43584e19a1c09cac67669b60e222c54a1295100f6a39813025bb3a4d`  
		Last Modified: Sat, 15 Feb 2025 00:40:02 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:0dd0842e343cd9f745bdebf8437f8fa942660088fd3c0e1ae9aa8f4be8a76243
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (318951861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1393759482bffe8fe51b3ab919abe11bf826f282f056b13f0179d330a9be1759`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Sat, 15 Feb 2025 00:40:12 GMT
SHELL [cmd /s /c]
# Sat, 15 Feb 2025 00:40:14 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 15 Feb 2025 00:40:15 GMT
USER ContainerAdministrator
# Sat, 15 Feb 2025 00:40:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 15 Feb 2025 00:40:17 GMT
USER ContainerUser
# Sat, 15 Feb 2025 00:40:18 GMT
ENV JAVA_VERSION=25-ea+10
# Sat, 15 Feb 2025 00:40:25 GMT
COPY dir:9943a6a8676ba9b798cfd35aa38f439443e45eb2bb7f1445736d316c89a33808 in C:\openjdk-25 
# Sat, 15 Feb 2025 00:40:30 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 15 Feb 2025 00:40:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8354e8b3669bda6a00bbeeed58438c1a7f531a76b878f7f2f72995dcf823efdd`  
		Last Modified: Sat, 15 Feb 2025 00:40:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a262ca6f514e1640d0dd8bc6ddba06dc304d7e92751625a939d873cc0cb91d`  
		Last Modified: Sat, 15 Feb 2025 00:40:34 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d758d9f27860a288b5b96e2634de8113edf4d126a9792919cfd76a5c9764be54`  
		Last Modified: Sat, 15 Feb 2025 00:40:34 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966ee492d86b47fc48c1cd8827ef08d48a92f95fe58b4e428065b16f574e4e02`  
		Last Modified: Sat, 15 Feb 2025 00:40:34 GMT  
		Size: 68.7 KB (68696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ce1ff1c8dc05dbc5e86c648420ee12c2bc90e677952708a7d2a44af93347f4`  
		Last Modified: Sat, 15 Feb 2025 00:40:33 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141f024f488ff60725701a1462597ed4c0f93f1619985c3839f0b33225ed2dfd`  
		Last Modified: Sat, 15 Feb 2025 00:40:33 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c851a61c5b5f2f55925884cc3fb7abb7fb169f59a926148c49eee81b97a014`  
		Last Modified: Sat, 15 Feb 2025 00:40:44 GMT  
		Size: 207.5 MB (207540327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cf15a0bcc21b87a2be5392518d4b064efaebae5d4bf0193f997bd6eabaca5a`  
		Last Modified: Sat, 15 Feb 2025 00:40:34 GMT  
		Size: 4.4 MB (4421116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9678d25ef8a5396b2f9a27a1bc586fa17ca48e0bb808c8408b060763ea2ada`  
		Last Modified: Sat, 15 Feb 2025 00:40:33 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
