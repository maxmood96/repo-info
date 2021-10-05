## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:78c8a20e0642aee138c377557e820dc44aba7bdc3d9f90ab8a90931c66c0c10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.230; amd64
	-	windows version 10.0.17763.2183; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.230; amd64

```console
$ docker pull eclipse-temurin@sha256:a69fecfb3873dde0dcc7260c73b70c7346d09644f245ddf530611aeccc5b822d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217207550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c41836a8bab57aa5265f1ca0cf5f67a18aee075c04647a4a2d79afa2f8d4609`
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
# Tue, 05 Oct 2021 22:18:25 GMT
COPY dir:6622177b1379d4d7267ebc9bc4d0bb013ea883bae36028c72b4045f7fa088598 in C:\openjdk-8 
# Tue, 05 Oct 2021 22:18:44 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:67c6ab93b4b418e5cbd36bba8f811ba69b13a66e76f43742c516faa5f74ac8f4`  
		Last Modified: Tue, 05 Oct 2021 22:35:15 GMT  
		Size: 100.2 MB (100164620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422092b74602a3accbabffe588a0df902d07c7e6cc73ec0fc667a0c7ad84a3de`  
		Last Modified: Tue, 05 Oct 2021 22:35:04 GMT  
		Size: 60.7 KB (60660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull eclipse-temurin@sha256:451979dd2a37322f0755c529adfbc5b98ee49902c75261cc30a50047a7d3dc0a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (203035330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094c9486ca0f3489d80fd1426be64c8f52733cf2cc8c84fbcd1086826178c9e3`
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
# Wed, 15 Sep 2021 16:20:56 GMT
COPY dir:6622177b1379d4d7267ebc9bc4d0bb013ea883bae36028c72b4045f7fa088598 in C:\openjdk-8 
# Wed, 15 Sep 2021 16:21:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:59e4e85af5a6b7877e699233aa0feb34db785873b96a3c1dc00ab4e9367a0a31`  
		Last Modified: Wed, 15 Sep 2021 16:41:17 GMT  
		Size: 100.2 MB (100169589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f9ae8aa819f22a71886d0121d7aa5e92b053e8e1ddb8e5134699733718f70`  
		Last Modified: Wed, 15 Sep 2021 16:39:32 GMT  
		Size: 89.5 KB (89539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
