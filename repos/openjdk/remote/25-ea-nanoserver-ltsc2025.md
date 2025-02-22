## `openjdk:25-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:32c04fdcfcdef523161ff8bc626bc92de5a139274b1fdbfcac48f94711414500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:25-ea-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:0aed7e810b8c6b7b98bfe24aae91c648e8847be48dae81f59a416517f0e4717b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.8 MB (406808571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06099005ca9ea02294615e2997283e5fbbfff002b7c76269f3299ace8a4ea730`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Sat, 22 Feb 2025 01:12:38 GMT
SHELL [cmd /s /c]
# Sat, 22 Feb 2025 01:12:38 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 22 Feb 2025 01:12:39 GMT
USER ContainerAdministrator
# Sat, 22 Feb 2025 01:12:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 22 Feb 2025 01:12:42 GMT
USER ContainerUser
# Sat, 22 Feb 2025 01:12:43 GMT
ENV JAVA_VERSION=25-ea+11
# Sat, 22 Feb 2025 01:12:50 GMT
COPY dir:d106a0277e031719ecf57df75fb675ae173cc670fca8c773deb70f0105f67fe7 in C:\openjdk-25 
# Sat, 22 Feb 2025 01:12:57 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 22 Feb 2025 01:12:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedcfe8af14abfa8266c1ec8f38a31b3676095ed2acf48451daffdf47ecf6557`  
		Last Modified: Sat, 22 Feb 2025 01:13:01 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c91fb1b0df7bc12ee8a32a3ae6d28182a485fd031a9a715c0cccb0722fc332`  
		Last Modified: Sat, 22 Feb 2025 01:13:01 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc0678bff4f0f793c4caacc28e2a8b9fc9b9d32294357abcf77ccb112bd2b37`  
		Last Modified: Sat, 22 Feb 2025 01:13:01 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947159b13511d8d0d559a11c5ee0e55d155d27a75f5007fb972893bd6af60a13`  
		Last Modified: Sat, 22 Feb 2025 01:13:01 GMT  
		Size: 76.3 KB (76288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105c9171ea104c7634ff5166bed915dc74c9f54af9b60acac404ca9690bfe681`  
		Last Modified: Sat, 22 Feb 2025 01:13:00 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e323c73d2bbfd79273674a1ff3a67bcdc36a49cb8289d24767ad8c0ebba9c3c1`  
		Last Modified: Sat, 22 Feb 2025 01:13:00 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d11396c3161e59ecda918454cdb5637216b69e8953f257374ebd8d7a03ada4`  
		Last Modified: Sat, 22 Feb 2025 01:13:12 GMT  
		Size: 207.6 MB (207571326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449eaf4ddc09d00f2b469c2601372c18cfe0f59bd99768747f3fa1c2d8c30673`  
		Last Modified: Sat, 22 Feb 2025 01:13:00 GMT  
		Size: 100.4 KB (100377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d305c170806d8ea72b7b17818f40fa4d4a37784edc34ab8794d931dc25a652af`  
		Last Modified: Sat, 22 Feb 2025 01:13:00 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
