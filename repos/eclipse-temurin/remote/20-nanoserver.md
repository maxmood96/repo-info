## `eclipse-temurin:20-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:728252c2edec44f3481ecbe832bb8ff2274b9edb0f8eaadf1e4f281750685abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1906; amd64
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:20-nanoserver` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:6db309aa826d119f5f9cb61b23b5a6943df92fd4da8a4f4275768a6c7bd45672
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316125381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713bdc5c499dd2f470dc169ad2f783adc2b0fef5a09206d60ffab43ae588d5ca`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:11:36 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 00:15:21 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Thu, 10 Aug 2023 00:15:22 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 10 Aug 2023 00:15:23 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 00:15:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Aug 2023 00:15:32 GMT
USER ContainerUser
# Thu, 10 Aug 2023 00:15:47 GMT
COPY dir:4ed074865171ba014f3c2f68f57ad2bb21a4dd6e4cf7ff9654ee6c4c6e5176c0 in C:\openjdk-20 
# Thu, 10 Aug 2023 00:16:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Aug 2023 00:16:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea9613880997b3ab2284a37c0c14a403553457b0c331b41c6bd6d1cc7838a222`  
		Last Modified: Tue, 08 Aug 2023 18:47:21 GMT  
		Size: 120.5 MB (120500677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3572ac06c9147f0946a40530f2197bb0101b82dd45b1defe04a8904a1c81a18`  
		Last Modified: Thu, 10 Aug 2023 00:30:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c858c43d3e6a9a3eff6b319404a1f9d4e8e209b3848f4ebe4844db5fe0a683`  
		Last Modified: Thu, 10 Aug 2023 00:33:12 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d07e124c511f04db80b6d58fd9332a9e6f0f6547d38cd19ea61f9d6555ff7`  
		Last Modified: Thu, 10 Aug 2023 00:33:12 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0274c2efbb42e692574088bbd3ca43b959d733d8c5466713050f9b0612ed0cac`  
		Last Modified: Thu, 10 Aug 2023 00:33:12 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959af0a666090aaf5f2e987624eb6b580fde01932e024dc30a16208a8010aa9f`  
		Last Modified: Thu, 10 Aug 2023 00:33:10 GMT  
		Size: 83.8 KB (83802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422f979be9d7f215d641f857cd4d38e61104c008a1487f17931f9c7f11977ecc`  
		Last Modified: Thu, 10 Aug 2023 00:33:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4b9078cfd257f89e567df589c43818ca8dd85b715b9492f372998f27b84961`  
		Last Modified: Thu, 10 Aug 2023 00:33:30 GMT  
		Size: 195.5 MB (195460015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23460c36860860fe35d8b2b873c5b5814b86b0b69f605bee4fb7222c0f65ac91`  
		Last Modified: Thu, 10 Aug 2023 00:33:10 GMT  
		Size: 74.4 KB (74442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bbe1a62a1ae0e615635eecf598f298c65966bed239aa386b15ac2f2da32685`  
		Last Modified: Thu, 10 Aug 2023 00:33:10 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:20-nanoserver` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:be60b529af41fa56590a8558d41687fd3ee220e274dc05bee08642790612786e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303780239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3390b5f677eaca292e3abc24164b420c4d711eef6b8f8c9930742e27f00de793`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 00:06:51 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Thu, 10 Aug 2023 00:06:51 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 10 Aug 2023 00:06:52 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 00:07:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Aug 2023 00:07:03 GMT
USER ContainerUser
# Thu, 10 Aug 2023 00:07:17 GMT
COPY dir:4ed074865171ba014f3c2f68f57ad2bb21a4dd6e4cf7ff9654ee6c4c6e5176c0 in C:\openjdk-20 
# Thu, 10 Aug 2023 00:07:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Aug 2023 00:07:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e08c5247c8c7d832882da17ac85015e9dd4d4dfc9e4114fc14746eb2abded`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9575234e65f0976570bdba51047c45b788c182e59a4a86efb4e30d4521c51d`  
		Last Modified: Thu, 10 Aug 2023 00:29:16 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96fa2722f8ce44a51817418af6adfc29ee0522f15f87ba911f83eae6afd62db`  
		Last Modified: Thu, 10 Aug 2023 00:29:15 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e8e732dea3e0c5045455018aca97c4e3956b4d16523e55434ddd09ced37551`  
		Last Modified: Thu, 10 Aug 2023 00:29:15 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b616fa9db00ddfffdc8a08b4b5b953c148cf5fac4aebf6fad6e93a366d2687`  
		Last Modified: Thu, 10 Aug 2023 00:29:14 GMT  
		Size: 68.4 KB (68432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1e05a9538fe6c1208075edbb290cd34f9912ad871f9bf68547fda8513874dd`  
		Last Modified: Thu, 10 Aug 2023 00:29:14 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44638f71a1a6d90f3eacdb32369c8ad9c5ebde7a46d6e950171b6fcfa7b49ad2`  
		Last Modified: Thu, 10 Aug 2023 00:29:32 GMT  
		Size: 195.5 MB (195464445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33046371120fbfbd709a1e3d26af280cf78ec1a838cab30cc8b5db18b8385f7c`  
		Last Modified: Thu, 10 Aug 2023 00:29:15 GMT  
		Size: 3.8 MB (3781023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c85f50cd5fd154bfe93caa4fe6437935c394cd68c8d55d49ad36842f29c25b6`  
		Last Modified: Thu, 10 Aug 2023 00:29:13 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
