## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a860df57798e491c7b52a1a30eb972629d634cc0581119dd21a94599a17837b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:d73253df0b44d8ad93682beb61fae16cc92d8e55f64d7788b60fb4afa27bde59
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321434068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7d860f662e5796e7dd8bf43cf56e7de98cec249e09b63355dfaa5cf7d9aad0`
-	Default Command: `["jshell"]`
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
# Thu, 10 Oct 2024 00:16:08 GMT
COPY dir:a4ffd7e89e4f3b2e7536e802b1dd43338b71e63559dd6ffcb51f99d655bc67fd in C:\openjdk-21 
# Thu, 10 Oct 2024 00:16:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Oct 2024 00:16:23 GMT
CMD ["jshell"]
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
	-	`sha256:3f60c53cb25ee367ee1f13f1cd4ba1abdd0f0cafa2428240589f07065e002013`  
		Last Modified: Thu, 10 Oct 2024 00:35:15 GMT  
		Size: 200.8 MB (200777135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce2c748fe78f99c3c0f7f00b00c148e934fff0cdb57856b7f03debc695b0895`  
		Last Modified: Thu, 10 Oct 2024 00:34:56 GMT  
		Size: 61.6 KB (61567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03f84315b2fe208c3bad470f819022d6fa878f9b9a1e3c394f440affff19f4`  
		Last Modified: Thu, 10 Oct 2024 00:34:56 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:c645fbd4284135490eb292549343c1298300010f0fb2443c725e423d7ee3e0ee
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359771375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf10f8205015fbb7bcf93b1a3dd2c5916f72baad956509b756b804209dcb272a`
-	Default Command: `["jshell"]`
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
# Thu, 10 Oct 2024 00:00:53 GMT
COPY dir:a4ffd7e89e4f3b2e7536e802b1dd43338b71e63559dd6ffcb51f99d655bc67fd in C:\openjdk-21 
# Thu, 10 Oct 2024 00:01:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Oct 2024 00:01:04 GMT
CMD ["jshell"]
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
	-	`sha256:97264187d612f0ecb60607efed1c87b424599a15e498cb360bbbd51db9947ee9`  
		Last Modified: Thu, 10 Oct 2024 00:29:41 GMT  
		Size: 200.8 MB (200777577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7fc62ea50f9a76e9b052f2f486c9c0d3b69827b6ed935ade699951707f3b1c`  
		Last Modified: Thu, 10 Oct 2024 00:29:23 GMT  
		Size: 3.8 MB (3825263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79718881876bf9e3faa2de1ee45f72ea30f7d21be4a4043a71f0f075cac2aa27`  
		Last Modified: Thu, 10 Oct 2024 00:29:22 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
