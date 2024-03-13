## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1919bb673453972e1168fcf40b4f416b91141a3edc5ba9cef6b5063df22f9592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.2340; amd64

```console
$ docker pull eclipse-temurin@sha256:49994c8b30696e1e99e82ce6cab33837a746f8ee9c3c9d111ff31761c8cdf998
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222556325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b30bb9f2d13dc73897ba20b177429142978ac3df2b1618a8c1c067770e2a0d0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 01:20:55 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 01:20:55 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 13 Mar 2024 01:20:56 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Mar 2024 01:20:57 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 01:21:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 01:21:11 GMT
USER ContainerUser
# Wed, 13 Mar 2024 01:21:22 GMT
COPY dir:9ab35a15e19e8247451d444f7de2a75fe407ec1749c1b49082dcaaef6c80dafd in C:\openjdk-8 
# Wed, 13 Mar 2024 01:21:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e98336f720b829e374bd1d59306210d3700861b11d3df51506afbc0b50d039`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c079b182eda7b2ab08c47e780f59a7b77e54541a35de305d05927577035b30b9`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6059e0fbeac8935bc15cc89e2b57e005314533c61cf3d4276b5e731fd46fef35`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8070e272015e9632bdda4cd151f601deeeb4345fcf61701d5133689cca3ed6`  
		Last Modified: Wed, 13 Mar 2024 01:40:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21dba345c47f39abd739524299d8d68413c670c39bccce29ba922fd4e548e735`  
		Last Modified: Wed, 13 Mar 2024 01:40:24 GMT  
		Size: 84.0 KB (83968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a06064b35b70fc8c4f626eb883a0d291ba26423f241de3f0ddb0f7cd83641`  
		Last Modified: Wed, 13 Mar 2024 01:40:24 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14e6dca7370deac3b79b79862161979dd348d700cb03604e784ce36c3282de`  
		Last Modified: Wed, 13 Mar 2024 01:40:36 GMT  
		Size: 101.7 MB (101701591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427515eee0dd740df8b15a89d7ef2ff9d045bedbea8778e7860468e7847c3064`  
		Last Modified: Wed, 13 Mar 2024 01:40:24 GMT  
		Size: 62.2 KB (62246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull eclipse-temurin@sha256:2471445e1a4933dec5ea8cbd9b1e49647c11f00a6bd2fedcc0194e6d50394d76
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206477877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f301120d567b411f405383ea37894c1368bc7d64dd5a698e5049bc35a1d333ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 00:41:38 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 00:41:38 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 13 Mar 2024 00:41:39 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Mar 2024 00:41:40 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 00:41:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 00:41:51 GMT
USER ContainerUser
# Wed, 13 Mar 2024 00:42:02 GMT
COPY dir:9ab35a15e19e8247451d444f7de2a75fe407ec1749c1b49082dcaaef6c80dafd in C:\openjdk-8 
# Wed, 13 Mar 2024 00:42:14 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9569a24b1d9b596a48436098ac5fe49c52e3153cd3bd147e365a80a4059570fd`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ac6979d3018020e5d56f24192e72d677112ce70959b875a73d0ceb74f7ab4a`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a09b00f17d16e8707c45a7f82c7b23111fc4386bb12c142f745c8f3d75630a0`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d598c02e10beef0b23187e3090a387054f0aaba86c9b427e0e59a2b6cf0375cf`  
		Last Modified: Wed, 13 Mar 2024 01:31:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df21f9058d8a1bfd11006bb0255f88c7865c2c34851a191447c198e670ea384b`  
		Last Modified: Wed, 13 Mar 2024 01:31:05 GMT  
		Size: 68.9 KB (68906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8255b1c5b4f751fb254a0543c26a87c06339f37b1f99fb38054529a1941b9`  
		Last Modified: Wed, 13 Mar 2024 01:31:05 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7179b12259b55aee7730300ceac3742f580f42d965894cdd49824bdc24c04001`  
		Last Modified: Wed, 13 Mar 2024 01:31:18 GMT  
		Size: 101.7 MB (101701462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a16ce7549abd7d18c55d766699875c4b83a0423280084fda7ac8ffa7d7e14a6`  
		Last Modified: Wed, 13 Mar 2024 01:31:05 GMT  
		Size: 81.6 KB (81606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
