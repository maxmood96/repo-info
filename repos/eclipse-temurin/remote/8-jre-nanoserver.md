## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a08cc6a62db07028673c9e5de4ca1964fb0b13f028b3454591a3e44c39d12c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.230; amd64
	-	windows version 10.0.17763.2183; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.230; amd64

```console
$ docker pull eclipse-temurin@sha256:d52a9c56518a62755070ad26909e96a637a6ee657ade07289e6759d6322c3857
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156116986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbb0d37ad3dfba0c44533a37acb664d5962d7566908cbe77ff419f52b20f360`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 06:44:45 GMT
RUN Apply image ltsc2022-amd64
# Tue, 05 Oct 2021 22:17:48 GMT
SHELL [cmd /s /c]
# Tue, 05 Oct 2021 22:17:48 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Tue, 05 Oct 2021 22:17:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 05 Oct 2021 22:17:50 GMT
USER ContainerAdministrator
# Tue, 05 Oct 2021 22:18:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 05 Oct 2021 22:18:13 GMT
USER ContainerUser
# Tue, 05 Oct 2021 22:19:04 GMT
COPY dir:1080d1f1dd1c0d61d0c45958055fb50fcd7599d7396f8e079867cfa7dbefbee8 in C:\openjdk-8 
# Tue, 05 Oct 2021 22:19:17 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:521b4ff1716af921a5cfbf2119d97dc479e9b1eb487d17d0f576ff856ab68e61`  
		Size: 116.9 MB (116897071 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:51c1c5356f69c33525116c868524e16b83d783420a64f7a7793348f61595daf2`  
		Last Modified: Tue, 05 Oct 2021 22:35:06 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc49703f7b56ae8d8a02566d2893a191a174788e3efc53fa4d9ea76f46a29a2`  
		Last Modified: Tue, 05 Oct 2021 22:35:06 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b92ec57dc477c59921d17feba55b7d77b4b0050e8687ca243edbc2ee41401eb`  
		Last Modified: Tue, 05 Oct 2021 22:35:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2792077d28d1cf8cd22686479116015a5408dc9efe47cde222be2701c5cd258`  
		Last Modified: Tue, 05 Oct 2021 22:35:04 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1c8deaea3916e765b026f0b9870aa409a2f0dee4f7f04d4f8f5d0d1fad25c3`  
		Last Modified: Tue, 05 Oct 2021 22:35:04 GMT  
		Size: 79.4 KB (79436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc00801257e7434447205cf90366dd6c9504305428e3a82144656cc7616532ee`  
		Last Modified: Tue, 05 Oct 2021 22:35:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb294bbf3e71bbb7297f18e85e3b620f6db6bb77df1b0adeb745befab87c9f6`  
		Last Modified: Tue, 05 Oct 2021 22:36:08 GMT  
		Size: 39.1 MB (39074037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c42c0471e23f4e43d56f586a700a3ca628559b5aaadd873554a9ba2cd34fca`  
		Last Modified: Tue, 05 Oct 2021 22:35:27 GMT  
		Size: 60.7 KB (60679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull eclipse-temurin@sha256:fd1dd1f27306a504c1843dd29f3747968dc5caac7525e999fd048401fbde39f3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141930090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5462080328d5f04b0f41b65163ce9b64d129de57a3b38645c9eef8feb93ff71c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 00:38:23 GMT
SHELL [cmd /s /c]
# Wed, 15 Sep 2021 16:20:33 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Wed, 15 Sep 2021 16:20:34 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Sep 2021 16:20:35 GMT
USER ContainerAdministrator
# Wed, 15 Sep 2021 16:20:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Sep 2021 16:20:46 GMT
USER ContainerUser
# Thu, 16 Sep 2021 19:15:43 GMT
COPY dir:1080d1f1dd1c0d61d0c45958055fb50fcd7599d7396f8e079867cfa7dbefbee8 in C:\openjdk-8 
# Thu, 16 Sep 2021 19:16:19 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:807d06303c39b2317729754a4c7ad6501e59c16ee464f8f671f9947774f62f72`  
		Last Modified: Wed, 15 Sep 2021 01:10:56 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5731adde04ee2252ac27813d5925fb91867aafd70d505dd0ee8c779d2f0861b0`  
		Last Modified: Wed, 15 Sep 2021 16:39:35 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ef075850bd103418d66728845f5b683d117cc72dc9975a5e22cb86e28bee97`  
		Last Modified: Wed, 15 Sep 2021 16:39:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007e224b123b02b7892d0aa9f4caf5a7c478f7d3e9792c9f21aa93237bf5da8c`  
		Last Modified: Wed, 15 Sep 2021 16:39:33 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe01989fb22d68a2c36e984344fc8dea4c076ab04d33fd563fd39da6048cb39`  
		Last Modified: Wed, 15 Sep 2021 16:39:32 GMT  
		Size: 67.1 KB (67119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987abbd4e696821e711d73f2dd27ceae2ccf2c0ae0d9478fa3422269b416f99c`  
		Last Modified: Wed, 15 Sep 2021 16:39:32 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a465fdb6f95f7b5967b411c42b2b0d4d1876cdcefff831b0520433e307842420`  
		Last Modified: Thu, 16 Sep 2021 19:23:50 GMT  
		Size: 39.1 MB (39074017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6735f57bf1bc349a0476011763da50ffc1a5236029034f6b24aff2192dc9551`  
		Last Modified: Thu, 16 Sep 2021 19:23:42 GMT  
		Size: 79.9 KB (79871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
