## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:c96bbc27ab294fa8d84e5f897b196575ae3a1a41af3f783a9bb0655142b7f227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:ef52dfb2d585356236fa106b4bc8ac7b75d2c16bb0a83289286632403bb2a414
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207213894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b93593bcadf391bd839fb5d7967f5bc6b91a0f6e9e967f8359bacd47b8eb67`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Wed, 09 Oct 2024 23:37:31 GMT
SHELL [cmd /s /c]
# Thu, 10 Oct 2024 00:00:25 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 10 Oct 2024 00:00:26 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 10 Oct 2024 00:00:27 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:00:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Oct 2024 00:00:36 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:04:18 GMT
COPY dir:6441dab14d212c21b2c8fcb6fc00e95950b0c66ee3c049dbfd71b18f09e541f6 in C:\openjdk-21 
# Thu, 10 Oct 2024 00:04:28 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6adfd98d9a05d48859cfa5f6e1dc162be56797c9e86e7647518192a16af3d27`  
		Last Modified: Thu, 10 Oct 2024 00:20:41 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901c8b373fdb2532b67bf4c385cb5acfe3bb3628a0b072bf19a4aba1d6642db1`  
		Last Modified: Thu, 10 Oct 2024 00:29:24 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a09d9b07073805bc7a0e3e9b65fab7f905866dab100ccaf4f0303a1e99d79d`  
		Last Modified: Thu, 10 Oct 2024 00:29:24 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2deb0292f49a0e20dfc31598486ba8943290c34db3daba7bbeeeeae3851241fb`  
		Last Modified: Thu, 10 Oct 2024 00:29:24 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adabf8dd66959c90add72005df2bd8830070884475d8b81696705b161570c56b`  
		Last Modified: Thu, 10 Oct 2024 00:29:22 GMT  
		Size: 68.1 KB (68127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0452ebf798fe976b987c3f00c4a87e715309bbae19f3e68510dd266200ccef`  
		Last Modified: Thu, 10 Oct 2024 00:29:22 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9547558733ee6d5f0ec56b82cb2c99d1d9ef97e1173440589c521d529e36da17`  
		Last Modified: Thu, 10 Oct 2024 00:30:40 GMT  
		Size: 48.7 MB (48665156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc456d5b62a72c3f375e6a0c1545e5602c60b0895ede15b03993f75f91633ff0`  
		Last Modified: Thu, 10 Oct 2024 00:30:32 GMT  
		Size: 3.4 MB (3381343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
