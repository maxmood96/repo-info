## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:75befdd37c9a199ecd5970dc50fb8485253f7fde8c6a1dfc9c5a22020e85772b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.230; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.230; amd64

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
