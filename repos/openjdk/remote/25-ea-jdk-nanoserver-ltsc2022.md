## `openjdk:25-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:7c63d18923418c18021565e04c6d724f190f9f468ddba090c5cb3a6a88a7f151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

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
		Last Modified: Tue, 11 Feb 2025 22:49:39 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f38ef4a01d2bc7b03f1c3ea02045fe94989f504c4d8e20e2ea6de9b6f4c282`  
		Last Modified: Sat, 15 Feb 2025 01:24:26 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e900c6c41211b58ea0e7b3d519d67211b3c518897f903e6bfb3c4ca5213f9e5f`  
		Last Modified: Sat, 15 Feb 2025 01:24:26 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da92c08a503e5796b262a6bb532526eab3d5004924618cc6c3ecfdd66110fe`  
		Last Modified: Sat, 15 Feb 2025 01:24:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f9f7d0459d13af107e20fcc7a3284c3e9b63522af77e40390e4965997d2fd`  
		Last Modified: Sat, 15 Feb 2025 01:24:26 GMT  
		Size: 76.1 KB (76059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96de596692c52791b0dc053a27fd4a0282808c7305b852c8d356ed7d14283b38`  
		Last Modified: Sat, 15 Feb 2025 01:24:26 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb8f1cad6810334966bd42109f78038d90c17ec23002becce553c57e276f6e`  
		Last Modified: Sat, 15 Feb 2025 01:24:26 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44b0da6b1c93e552c4b92c8f4bbbc3bbb905476fb677a0868cb6fe8365e6620`  
		Last Modified: Sat, 15 Feb 2025 01:24:41 GMT  
		Size: 207.5 MB (207540800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8a36cc5bd22085114918b500546b42c03e830d00d7b4aa9a118e454a6f0c8f`  
		Last Modified: Sat, 15 Feb 2025 01:24:26 GMT  
		Size: 118.4 KB (118401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3dcf8c43584e19a1c09cac67669b60e222c54a1295100f6a39813025bb3a4d`  
		Last Modified: Sat, 15 Feb 2025 01:24:26 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
