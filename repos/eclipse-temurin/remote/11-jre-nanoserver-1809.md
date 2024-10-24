## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:6e715d530e12fc08f0bc2bf8d654968d6b4306576093786f39459e4c06bb7e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:bc9814562b63a463b575d32cd24e657462a84f7034b25bceab3642eea3c6f62a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199541471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8830687406e60ad8debe4b9c4318cb7a2a5eb874c81735718d78f4e73645d18`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 24 Oct 2024 01:53:13 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:53:14 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 24 Oct 2024 01:53:15 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 24 Oct 2024 01:53:15 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:29 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:35 GMT
COPY dir:a15dacd11bbcaacf83a6b6e1490d6483ae4af68a125407fd4cb6bb7a70e4639c in C:\openjdk-11 
# Thu, 24 Oct 2024 01:53:39 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09955945e4362240c347d12734c2ce1f7b26f5e1d6c71e6d3caa906d4ae03d7a`  
		Last Modified: Thu, 24 Oct 2024 01:53:42 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ec4fb7cf7ecfbc2fa4b2d5405a6bdb4c0450c4929fd73771bb6708fb001c93`  
		Last Modified: Thu, 24 Oct 2024 01:53:42 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd986792cee49d0d1329139dcc593dd45ed97fbbbd24b825e0d2ff923b149650`  
		Last Modified: Thu, 24 Oct 2024 01:53:42 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b3e008b66da69dd52cccb466daccccd09ad8970c280255249c217646e78a7a`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d69d8d282cbd2ef76241b2505298bfcd6f418e12da2dae16fb5a057e2ed0e3`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 65.8 KB (65844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c581a463455842b187856b3f6de877e1ed8d6c6c02b21cdf1371e17ff72f29bf`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a0fec843b5fc61346ac07a3a38aa76224c6242183e3d6e1d099f86e24f58bf`  
		Last Modified: Thu, 24 Oct 2024 01:53:46 GMT  
		Size: 44.3 MB (44308612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cf8c3ace80a4394c0af9825cbbfe57e55bb52d01e6e80889773b880d09b71e`  
		Last Modified: Thu, 24 Oct 2024 01:53:42 GMT  
		Size: 68.2 KB (68188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
