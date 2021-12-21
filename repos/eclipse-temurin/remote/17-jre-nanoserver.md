## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:843cb264dcf900fea9575ae6f1eb3b5f13a51a254d263d6126cde783dd77329e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.405; amd64

```console
$ docker pull eclipse-temurin@sha256:12648210cbeffc8e9f429a78847ec702766f4fdc4c63a3c2712b3021953c456c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160447708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfd17b8444461a1fcbfacea8df3a59eb984b2599e84e604d9d36b05485ab4f0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 08 Dec 2021 01:24:33 GMT
RUN Apply image ltsc2022-amd64
# Sat, 18 Dec 2021 06:03:19 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 06:06:04 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Sat, 18 Dec 2021 06:06:04 GMT
ENV JAVA_HOME=C:\openjdk-17
# Sat, 18 Dec 2021 06:06:05 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 06:06:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 18 Dec 2021 06:06:16 GMT
USER ContainerUser
# Tue, 21 Dec 2021 18:27:15 GMT
COPY dir:38eebe4e3a4da98e178f49482de333d171d427f5886e68b2b67715641b9694d5 in C:\openjdk-17 
# Tue, 21 Dec 2021 18:27:35 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:11961e4f2e13a442b572d4bc37edfe94ad6d8c2ed378f0dcae8b880959c4b538`  
		Size: 117.2 MB (117225770 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:29e118c52df9d671b57a04fe35f79f686c3a7038ccd41c5bf5ccfac737426ab6`  
		Last Modified: Sat, 18 Dec 2021 06:41:30 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e811ecc0798c7f5b5d446d99777a44e54378e606a0323328a83423e23aba09de`  
		Last Modified: Sat, 18 Dec 2021 06:48:24 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da45c2d31b5896f97988806b3a81e6859c7b8752c37c86c28413e7d5f4f81c65`  
		Last Modified: Sat, 18 Dec 2021 06:48:24 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10dd6f14c8776f772735798c6d11effbd00c1beeaa404fa968712d54da52c83e`  
		Last Modified: Sat, 18 Dec 2021 06:48:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45550c42552ede4d9b7a2fe54baa3330d4a9ae3514d58fe9f85cbc3004daea7c`  
		Last Modified: Sat, 18 Dec 2021 06:48:22 GMT  
		Size: 79.8 KB (79780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980420ec3f66e69980daff785f80abf94c28d80a86ff05d22129eef320268bfb`  
		Last Modified: Sat, 18 Dec 2021 06:48:22 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a44967263da51a9bd31c2feaec9595133482617fda96e066f597b9d7e6ab35`  
		Last Modified: Tue, 21 Dec 2021 18:32:05 GMT  
		Size: 43.1 MB (43075633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e878baa845f3dca2e6f5ef93819377d069ff8f0f6375bac9ff416802b1e56eaa`  
		Last Modified: Tue, 21 Dec 2021 18:31:56 GMT  
		Size: 60.7 KB (60744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.2366; amd64

```console
$ docker pull eclipse-temurin@sha256:8e7958f2fa4b3ff7a4dd062c35749c773e402dc15ca0e0444c06d142a1fe9957
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149069869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32db7a644f23aac9b509ba9143fd3329c9f27fd2723e997e53b44f69ac48935`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 05:18:44 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 05:58:50 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Sat, 18 Dec 2021 05:58:50 GMT
ENV JAVA_HOME=C:\openjdk-17
# Sat, 18 Dec 2021 05:58:51 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 05:59:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 18 Dec 2021 05:59:05 GMT
USER ContainerUser
# Tue, 21 Dec 2021 18:22:44 GMT
COPY dir:38eebe4e3a4da98e178f49482de333d171d427f5886e68b2b67715641b9694d5 in C:\openjdk-17 
# Tue, 21 Dec 2021 18:23:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4c557aac927613dd487d7c04b01a8eeb8ad174693f61b14c8f4285f1db6afdd2`  
		Last Modified: Sat, 18 Dec 2021 06:13:05 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26306f8e8a4f4dfe20500528de7aa39df4e7dee0979f58489a2ded09004ffbd`  
		Last Modified: Sat, 18 Dec 2021 06:40:15 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9362cfac01213205fa1c339e140a340bb1905cb5e0a78c93e0c6a0e5bbfef6d0`  
		Last Modified: Sat, 18 Dec 2021 06:40:14 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec169fd6feabc29f6922c4666746164f5167e3d65707e55174b9a8f12cabf094`  
		Last Modified: Sat, 18 Dec 2021 06:40:14 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0099d82d3944a044d664e71f334526a8d7d2ed1bd7096d3acb142c80c2ea7bb7`  
		Last Modified: Sat, 18 Dec 2021 06:40:12 GMT  
		Size: 66.9 KB (66924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0ed6216ade0a806a34dbf8eed2a100bee72f70e7f01a8403826a5a189e8e6b`  
		Last Modified: Sat, 18 Dec 2021 06:40:12 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd46bfa6b024452cf4983a58884281a3eb2ebfd699c45830629da9acd5c9262a`  
		Last Modified: Tue, 21 Dec 2021 18:31:19 GMT  
		Size: 43.1 MB (43072404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122c9ccdc8d62f2bfc14782e1395317a7926221c18b675ec48ff0fb83239a319`  
		Last Modified: Tue, 21 Dec 2021 18:31:11 GMT  
		Size: 3.0 MB (3020728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
