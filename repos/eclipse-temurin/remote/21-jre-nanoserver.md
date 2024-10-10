## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:fff26dcaa06aaeafcbb30e48f336429f6421230b6c93901c583bd4a54345d83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:08b67ea54f664031f32e03d7b29caf9f695d4a1979c74ffb2d22f9d16acd054e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169321073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74cfcd328acc397fe0f58a6bd5ac7d7c5d81dc6e54e96220b722ef886827dac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:11:44 GMT
SHELL [cmd /s /c]
# Thu, 10 Oct 2024 00:15:42 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 10 Oct 2024 00:15:43 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 10 Oct 2024 00:15:44 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:15:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Oct 2024 00:15:54 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:16:42 GMT
COPY dir:6441dab14d212c21b2c8fcb6fc00e95950b0c66ee3c049dbfd71b18f09e541f6 in C:\openjdk-21 
# Thu, 10 Oct 2024 00:16:54 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96818114ce85fcf68e8af61951767bf11ed374ffe6a9023b6150122fbad46d51`  
		Last Modified: Thu, 10 Oct 2024 00:32:47 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4381491f7a621ef132d497c650d372228e1972466ed342d9b253bb8f8696a99`  
		Last Modified: Thu, 10 Oct 2024 00:34:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbeda7b20a180c15ea2662bc0f428e75aeeef3bbfbcc6ee3d2f0ea2c57824f0`  
		Last Modified: Thu, 10 Oct 2024 00:34:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20825ba114810a7a5938603953ac3cd5926bc7735726a8781ebcf79bac79ba17`  
		Last Modified: Thu, 10 Oct 2024 00:34:58 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df05ef02b28f3298c5b68b730abf5da2175b95061afb183d6d7d405e0c218f94`  
		Last Modified: Thu, 10 Oct 2024 00:34:56 GMT  
		Size: 77.5 KB (77533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e53603dbfba3bc09f2ee9a4f12315be3fdca7ed1df65854abb2122bbb9c204`  
		Last Modified: Thu, 10 Oct 2024 00:34:56 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0b673edde38e7b6153fd8c0406edcce76ac3a9c51f9c6a783f65fbf08d4be3`  
		Last Modified: Thu, 10 Oct 2024 00:35:34 GMT  
		Size: 48.7 MB (48665270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc7e4db586e3a4ff8be74eb0539dde71c67f860974689ce6269fe169f273bc5`  
		Last Modified: Thu, 10 Oct 2024 00:35:25 GMT  
		Size: 61.6 KB (61574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.6414; amd64

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
