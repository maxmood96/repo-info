## `eclipse-temurin:11-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:eb7194c7b9efe761b57df57a4a1d06378f8b7a01a1f60506c032fee6327d48e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:b7f76d7f75d58ddf4150152b132b27a72f48aa46afcd8b086c050e3078b6ef1c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237885075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8b9d5f3e4c2e024282f134f7a017ca266f503053531a8104293ce9b86aed55`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Sat, 08 Nov 2025 19:18:07 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:18:08 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 19:18:08 GMT
ENV JAVA_HOME=C:\openjdk-11
# Sat, 08 Nov 2025 19:18:08 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:18:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:18:15 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:18:23 GMT
COPY dir:4835e564d5b678d207d3850b6f40a90e0afa12e9d665c48e7909a88923b1a7a8 in C:\openjdk-11 
# Sat, 08 Nov 2025 19:18:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3edcb81db944e3d99610961c9e1ebcb1d8a1a26921ce049083bd40166e3a3e3`  
		Last Modified: Sat, 08 Nov 2025 19:18:42 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc67a3aa7924e31f7e97be0914fe2b01a4017f7639f5d8defa7386f5ecf2057f`  
		Last Modified: Sat, 08 Nov 2025 19:18:42 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2be747439e23f2e09688d0498e4c6c32f29f851dc660b2a686e3f447734709`  
		Last Modified: Sat, 08 Nov 2025 19:18:42 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2419151e27cc7b59bac3f937860a4a5d633d5ab0c4e5519d075ab3873f6b79`  
		Last Modified: Sat, 08 Nov 2025 19:18:42 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7d3e791536cb34e666192ac7766afe2a504b03d0af6483c15b43d83a15c1d5`  
		Last Modified: Sat, 08 Nov 2025 19:18:42 GMT  
		Size: 69.9 KB (69933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaecb949a551591cfad6066ebe505fafdf42270a91b086e2dc0e8f6dec45d99`  
		Last Modified: Sat, 08 Nov 2025 19:18:42 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510d433bedec3af4c226bf936934b622cabc02d73c05eafe1602cb56fccf5b26`  
		Last Modified: Sat, 08 Nov 2025 19:18:52 GMT  
		Size: 43.7 MB (43694939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48b4fc610314f4dc7dc2d95d040b7a185a24a7aeaca27f987fe44a61c0fb3ae`  
		Last Modified: Sat, 08 Nov 2025 19:18:42 GMT  
		Size: 85.5 KB (85507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
