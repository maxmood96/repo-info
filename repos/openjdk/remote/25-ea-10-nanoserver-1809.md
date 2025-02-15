## `openjdk:25-ea-10-nanoserver-1809`

```console
$ docker pull openjdk@sha256:0dc8fbb5e574cbc353ef3d776f2298781eb788b72891fde7fd256301a1295a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-ea-10-nanoserver-1809` - windows version 10.0.17763.6893; amd64

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
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8354e8b3669bda6a00bbeeed58438c1a7f531a76b878f7f2f72995dcf823efdd`  
		Last Modified: Sat, 15 Feb 2025 01:24:25 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a262ca6f514e1640d0dd8bc6ddba06dc304d7e92751625a939d873cc0cb91d`  
		Last Modified: Sat, 15 Feb 2025 01:24:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d758d9f27860a288b5b96e2634de8113edf4d126a9792919cfd76a5c9764be54`  
		Last Modified: Sat, 15 Feb 2025 01:24:25 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966ee492d86b47fc48c1cd8827ef08d48a92f95fe58b4e428065b16f574e4e02`  
		Last Modified: Sat, 15 Feb 2025 01:24:25 GMT  
		Size: 68.7 KB (68696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ce1ff1c8dc05dbc5e86c648420ee12c2bc90e677952708a7d2a44af93347f4`  
		Last Modified: Sat, 15 Feb 2025 01:24:25 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141f024f488ff60725701a1462597ed4c0f93f1619985c3839f0b33225ed2dfd`  
		Last Modified: Sat, 15 Feb 2025 01:24:25 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c851a61c5b5f2f55925884cc3fb7abb7fb169f59a926148c49eee81b97a014`  
		Last Modified: Sat, 15 Feb 2025 01:24:39 GMT  
		Size: 207.5 MB (207540327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cf15a0bcc21b87a2be5392518d4b064efaebae5d4bf0193f997bd6eabaca5a`  
		Last Modified: Sat, 15 Feb 2025 01:24:26 GMT  
		Size: 4.4 MB (4421116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9678d25ef8a5396b2f9a27a1bc586fa17ca48e0bb808c8408b060763ea2ada`  
		Last Modified: Sat, 15 Feb 2025 01:24:25 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
