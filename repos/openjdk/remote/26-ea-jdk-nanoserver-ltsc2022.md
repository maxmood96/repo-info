## `openjdk:26-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:186b4437142e920913686c7c3ec5f560b248fe0bf8557567b03915f6dcedb0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

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
