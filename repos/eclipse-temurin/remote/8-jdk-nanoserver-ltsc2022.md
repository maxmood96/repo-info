## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9be3b3487b79575b81c804b9cd5a2f10e926dbd71abb62110a0b838647f3bf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.230; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.230; amd64

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
