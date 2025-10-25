## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7e34da0dd7f2787ab18ea85ff51f31046f04911510bf3969ae0d0d4a4b45d7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:a78326388e9a34ca156a511feffb8d05f8807ef09bb8aea2de80914cd68d0fb2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.0 MB (237981207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d624854d44040a0f5668f06d9fa62782a883b1f4b1e19fb6fe95165fe120976`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 19:21:57 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:21:58 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 24 Oct 2025 19:21:59 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 24 Oct 2025 19:21:59 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:22:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:22:05 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:22:11 GMT
COPY dir:f06eb607ed2664f134ec9f1021e1b4f935a771c666407ab724ddde53439bca46 in C:\openjdk-17 
# Fri, 24 Oct 2025 19:22:15 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b542e72135d0534ba79da2a41d1f60f4d1969628fc8610750e767a0e31da1`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750f9a838c7f467f4af45e57f9bcb67f003d54710327ac492573342ad87069b2`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099cdc743bf58bcf3024b743aff0ffd112471c3f731bf8794e988bb3519ac7c3`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fdbac106f97e9e17f8c27bcfdbb9fecad0b1d5801b43c738782f189d6210f9`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24486d2b0e77691c0820f16e5482874dbe3d234e18318e064ead0fd949a908f`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 83.4 KB (83435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc265f8ea29f7d65785c19c8a9641bef9b63cb8a62d38be8c04e83d67dd08cf`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83215d101470f8eda83f7daeac6428f52646b77185f0dea898ff3c683a438496`  
		Last Modified: Fri, 24 Oct 2025 19:23:21 GMT  
		Size: 43.7 MB (43748284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a6b53e482039579c8ceff56c64712db181e6654a5c99bc05fb600bc176bacc`  
		Last Modified: Fri, 24 Oct 2025 19:23:17 GMT  
		Size: 114.7 KB (114748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:1620b806f8fe971e2ba2e7422bc6c1b02c45190837d8dd4ea44dd0b180281e27
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166622420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd58dfcbb7c3194187b7d64266ec579a434d51b4866c9f7c896945f4c1bfe38`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:19:18 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:20:42 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 24 Oct 2025 19:20:42 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 24 Oct 2025 19:20:43 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:20:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:20:46 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:22:14 GMT
COPY dir:f06eb607ed2664f134ec9f1021e1b4f935a771c666407ab724ddde53439bca46 in C:\openjdk-17 
# Fri, 24 Oct 2025 19:22:18 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde8d3892490c03c6867f198f3dc45e69fe1049b2d63e6fc8a4a21f54095e87d`  
		Last Modified: Fri, 24 Oct 2025 19:20:16 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9581df62aaaf2a6a24830901fbfc0bac2faa74046ee41e8b9da720538647aeb`  
		Last Modified: Fri, 24 Oct 2025 19:21:40 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03290cac1f030e1eedde31a38d5cb12f78dd8b0a60078b719dcea75100524c3f`  
		Last Modified: Fri, 24 Oct 2025 19:21:40 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe8f0ed4aa237a5f1a4785841a222a9ed1e197475726bb88704851892893cbf`  
		Last Modified: Fri, 24 Oct 2025 19:21:40 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33febd4530edf0a14d178e5dcb80bbe021598e635ad30f7add8e3ac3314fde37`  
		Last Modified: Fri, 24 Oct 2025 19:21:40 GMT  
		Size: 76.7 KB (76684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a7e5d60108d2a76abe3bdcddeece786acaf05cf3ca918cfbd60c901aed18e6`  
		Last Modified: Fri, 24 Oct 2025 19:21:40 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a679d108c4e69c824f7a3bd73bdf8fd689b63e48e83804c9704179e02e22759d`  
		Last Modified: Fri, 24 Oct 2025 19:22:37 GMT  
		Size: 43.7 MB (43748237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59e74141dc085e94cd58d6c8d3a824a4e26e089b50fc38f83f0123a34d00402`  
		Last Modified: Fri, 24 Oct 2025 19:22:33 GMT  
		Size: 108.1 KB (108084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
