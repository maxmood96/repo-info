## `openjdk:21-ea-25-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:2283d6c886ea2de298d5de301ab5697071d36b3c4490881804a2fb52b68df85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `openjdk:21-ea-25-jdk-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull openjdk@sha256:3a6416f3042850913a1c853ecd23c72722b4cf1c9284b6fab99b630746d83215
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (306047233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74867afe6b21539a377325e1e14701f0079b8caf6eda87f604ddb04bb07d5fb2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 00:40:01 GMT
SHELL [cmd /s /c]
# Wed, 10 May 2023 02:57:56 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 May 2023 02:57:56 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 02:58:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 May 2023 02:58:09 GMT
USER ContainerUser
# Thu, 01 Jun 2023 23:18:34 GMT
ENV JAVA_VERSION=21-ea+25
# Thu, 01 Jun 2023 23:18:50 GMT
COPY dir:a3e22bc9f0f48f48e47a48a315f64efb2956f2ff8ee30391c9ac1e79a90b5d98 in C:\openjdk-21 
# Thu, 01 Jun 2023 23:19:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 01 Jun 2023 23:19:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b79dd15c5dd82bc10521b9a4e49241f70088bc6edbb286f90be198abea55e23`  
		Last Modified: Wed, 10 May 2023 03:01:27 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40d6657961af59b636be2db4aa1fcef304eb245271a8ae41504adce8615cd1d`  
		Last Modified: Wed, 10 May 2023 03:01:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906b9562d5b2a03bb6c35a1ad6ee0d9becffcc133bb4d938b390c69e08ed9ed`  
		Last Modified: Wed, 10 May 2023 03:01:26 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa4992dcb0ef11fcada4b2f46b4a9c8cde731d43e793119cd32bd5fed253cd8`  
		Last Modified: Wed, 10 May 2023 03:01:26 GMT  
		Size: 66.9 KB (66929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee642db739fb63532d81702ffb8160c34a27c60b4725dcea8a48eae94769a63`  
		Last Modified: Wed, 10 May 2023 03:01:24 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe67b90a0a32337c92c94a50ecbb4be2d3bfed31ddb4218313bb514ced93058`  
		Last Modified: Thu, 01 Jun 2023 23:21:06 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731281e8a9226e8b762251d47fc08918dca8892208697ec9e89b43d4f5bc958a`  
		Last Modified: Thu, 01 Jun 2023 23:21:26 GMT  
		Size: 197.8 MB (197780671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1a4e11149b54e892eeff2f9b1f4dddf3b5b5db6f0d107bec6eddce08163e78`  
		Last Modified: Thu, 01 Jun 2023 23:21:08 GMT  
		Size: 3.8 MB (3808717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deebd7ae03735eaa559b796fee1c355576fa22e73c3b46c728b9d84c1657a04`  
		Last Modified: Thu, 01 Jun 2023 23:21:06 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
