## `openjdk:26-nanoserver`

```console
$ docker pull openjdk@sha256:b52c797f6c806995df31344f74f0a0d381ef4d3710cfdfd8f67adc1a58c217b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:c6238a69442570834374763d8a1781b39c15d1928df5ba5fa536b8c9a70cc6b7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.4 MB (415383544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450b5c3ff33a2ae9175d31901a5d971f680e627eefc5098f761d55b33c0165b4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 19:20:51 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:22:24 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 24 Oct 2025 19:22:24 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:22:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 24 Oct 2025 19:22:26 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:22:26 GMT
ENV JAVA_VERSION=26-ea+20
# Fri, 24 Oct 2025 19:22:38 GMT
COPY dir:6bffdfd50160c82e6869fd0a690d084eedfe2bd58671ef19a440f7d2cd9a5727 in C:\openjdk-26 
# Fri, 24 Oct 2025 19:22:43 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 24 Oct 2025 19:22:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8407703267a708f1e861d96ba7297b491ec4181f89a12fcf487a7b283523fd8a`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d049885f1168820d10689dd2a9b31272ab9b90fd4afe0e42ac7d201fc2634562`  
		Last Modified: Fri, 24 Oct 2025 19:23:17 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae075814f368a1aa2b03f2b072513d1a6ebb97b81c8ae08dffaaf673cee2e17f`  
		Last Modified: Fri, 24 Oct 2025 19:23:18 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf71f4e56980b0dfb80e1853c73eca005f0a2e5f2a1279427e6c3c37e9de53cf`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 72.1 KB (72108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e598fd04f697b70b20b173383d3399c6279de834e511631457c0c257fc0f95`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0900502dd016e7205278d4b7f5c0866bfbaf45e2d3b8423a56f3c5309c0c6213`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910e63b9d4989aeb9fb9ec1e8b1927705af0d813f518e3b8b5137fa984754f35`  
		Last Modified: Fri, 24 Oct 2025 21:24:39 GMT  
		Size: 221.2 MB (221151933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6be36a899281814aea046b135690305be2396eda7af2cd78585a20439bf551`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 123.6 KB (123637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8c4bc730d1794f83b9eaf05395a6ded49f06aa10cc319aaab9220782472100`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-nanoserver` - windows version 10.0.20348.4297; amd64

```console
$ docker pull openjdk@sha256:1012f70d32eb95f4469647a7f71b53056b3b67f5ee5b14755edf514c2b85ac68
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (344048636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8ac51f20d69b44aed834633546aee1ef9a3e26693f06cf19244113235bde87`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:09 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:21:10 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 24 Oct 2025 19:21:11 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:21:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 24 Oct 2025 19:21:19 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:21:20 GMT
ENV JAVA_VERSION=26-ea+20
# Fri, 24 Oct 2025 19:21:59 GMT
COPY dir:6bffdfd50160c82e6869fd0a690d084eedfe2bd58671ef19a440f7d2cd9a5727 in C:\openjdk-26 
# Fri, 24 Oct 2025 19:22:07 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 24 Oct 2025 19:22:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8999c939624fe677d0d91b87b1126c4f89d739dd83e7f1cc49c18df4f1bcdff8`  
		Last Modified: Fri, 24 Oct 2025 19:22:57 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9d2395da7e2f2e68218fb4a0b66131745120a80cb74f35dec92913a8d8828d`  
		Last Modified: Fri, 24 Oct 2025 19:22:57 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6beb3f249899d034a719424b6fd288649f6bea0530dfac718f68efbea11abe54`  
		Last Modified: Fri, 24 Oct 2025 19:22:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b348bf97b8fef52dac27eca7bb63cf001d4e4c74c7922843c345620ef36603`  
		Last Modified: Fri, 24 Oct 2025 19:22:58 GMT  
		Size: 70.8 KB (70783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a4f51773b750337d56dc99c920f188458c36cf267d826e62f098d431c1ed3a`  
		Last Modified: Fri, 24 Oct 2025 19:22:57 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06ad009d79e5fc6e770bea2f162ff5f2335f44c359f2f60692dfcbbfc281942`  
		Last Modified: Fri, 24 Oct 2025 19:22:58 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4afd5021e5d50ca40b5941dde34901e0fcf19fe8accc286e92c3dd687867a7`  
		Last Modified: Fri, 24 Oct 2025 21:24:02 GMT  
		Size: 221.2 MB (221152329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b60b04509dc6861d42747456b509ccb30915282f20d81b7777b11befc9ff737`  
		Last Modified: Fri, 24 Oct 2025 19:22:58 GMT  
		Size: 135.1 KB (135117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d04db77e7466651450dd863ef4b7d8df628acdcded2162e11f25bda71a9eae2`  
		Last Modified: Fri, 24 Oct 2025 19:22:57 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
