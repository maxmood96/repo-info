## `openjdk:27-ea-nanoserver`

```console
$ docker pull openjdk@sha256:d3f3feeb9f0a342209a37a72b5a754ba86d04a492cfdbb9e2661c48ffec9ab7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-nanoserver` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:035fa17a1f0e238307c38e0f18a1d62ef52569ddee79ec5cda286292aa8b32d1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.9 MB (423865305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b99e3341f5a85f694dce78599d5aff3bbb7c3da5d01e6dff46991f66c75976d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 17 Feb 2026 20:08:39 GMT
SHELL [cmd /s /c]
# Tue, 17 Feb 2026 20:08:40 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 17 Feb 2026 20:08:41 GMT
USER ContainerAdministrator
# Tue, 17 Feb 2026 20:08:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 17 Feb 2026 20:08:52 GMT
USER ContainerUser
# Tue, 17 Feb 2026 20:08:52 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 20:09:11 GMT
COPY dir:625a2d1f532d621a6c743669def3255030013f9f8e2976a431958fd4473522f3 in C:\openjdk-27 
# Tue, 17 Feb 2026 20:09:19 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 17 Feb 2026 20:09:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fc17a1f469c0eadfd8cfd4f8bf797b03f6d52135851c82505c393c1d834e44`  
		Last Modified: Tue, 17 Feb 2026 20:09:26 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e19c21f86adbccaec2ff72c8705a7f19427f420102b44ce6b31585fdc56c9ba`  
		Last Modified: Tue, 17 Feb 2026 20:09:26 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be2f94be82e7abb1f548564d719a2f3062740c0473bf8002eff6828692773b`  
		Last Modified: Tue, 17 Feb 2026 20:09:25 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac1e6d509efe5bc5d81c61ffe5a0b7face26e7e5bec0b2059c88d2b9f880b4`  
		Last Modified: Tue, 17 Feb 2026 20:09:25 GMT  
		Size: 70.0 KB (69993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d926350d75e3be64410cc50621d39ed4a7082de0011128774b234de77d76c79`  
		Last Modified: Tue, 17 Feb 2026 20:09:24 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec133a471510a2c2362188575b4bd59237c76a0f7669839770f643c946db7915`  
		Last Modified: Tue, 17 Feb 2026 20:09:24 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f254aca52fb9ea7dcfd30e0f62b8d48906f285c741a3a5558df3ecb98366561`  
		Last Modified: Tue, 17 Feb 2026 20:09:40 GMT  
		Size: 224.4 MB (224433941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb526eaec58873a30a044ec5258fdc1e70ee2b75a99f1498b6da5d9674145e1f`  
		Last Modified: Tue, 17 Feb 2026 20:09:24 GMT  
		Size: 103.4 KB (103377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24cc521ef471fde413d6b7c107e498aec8a9a9a34e97f7b79bc412904fc15cd`  
		Last Modified: Tue, 17 Feb 2026 20:09:24 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:3fd81fdd59644c4a01630c6ae38d785550bad5684c6a5aa791fd9b29bb45f987
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351272284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2479ca0fd7fd306175e9c33331e097a15144dc3908842460d01d163c51ec9ba7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 17 Feb 2026 20:11:58 GMT
SHELL [cmd /s /c]
# Tue, 17 Feb 2026 20:13:56 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 17 Feb 2026 20:13:57 GMT
USER ContainerAdministrator
# Tue, 17 Feb 2026 20:13:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 17 Feb 2026 20:13:59 GMT
USER ContainerUser
# Tue, 17 Feb 2026 20:14:00 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 20:15:28 GMT
COPY dir:625a2d1f532d621a6c743669def3255030013f9f8e2976a431958fd4473522f3 in C:\openjdk-27 
# Tue, 17 Feb 2026 20:15:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 17 Feb 2026 20:15:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9133238e3559d47b254a3443555b690c1c826f76a8aa04c2132fa0a227e81e`  
		Last Modified: Tue, 17 Feb 2026 20:13:26 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263a0d895562884df3b124d8d6fc3f0e82a3e25ea02b49002b07be3644412400`  
		Last Modified: Tue, 17 Feb 2026 20:15:42 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dac68683f4d9eee7be14442a9b580f10c5cf8739e87af5898e8ca9529718a19`  
		Last Modified: Tue, 17 Feb 2026 20:15:42 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b470d3a48a00eda2c3573c93288ac3499258fc01d64c5b6953d4dcd37c173517`  
		Last Modified: Tue, 17 Feb 2026 20:15:42 GMT  
		Size: 78.3 KB (78261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0fe5f69e8fa11f5c049bbe2fe88e276acd95adbd38599e56c1f73f2b579b23`  
		Last Modified: Tue, 17 Feb 2026 20:15:41 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fdff33eba67de48a8a4138f34a76e7ad3649eda2c848f7f7b75f3c6b228241`  
		Last Modified: Tue, 17 Feb 2026 20:15:41 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e2e87f10a9b7bdd1ca7bdb78973a32ba3cef715e6805695004a758d0e8086a`  
		Last Modified: Tue, 17 Feb 2026 20:15:56 GMT  
		Size: 224.4 MB (224434736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99193e6a9eec15bf270bfb47f4a84cbb1614b743e9f9b70bd56ec865b841303`  
		Last Modified: Tue, 17 Feb 2026 20:15:41 GMT  
		Size: 107.1 KB (107100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62be9163543ea67e2122466765446504b82e37685001414b69b3061859b48e6`  
		Last Modified: Tue, 17 Feb 2026 20:15:41 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
