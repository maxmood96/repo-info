## `openjdk:26-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:d0e6a78a68f479942f2004baffc2b4eace85293bf342f3774eeff7e9b472f047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `openjdk:26-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:0dfadb33f067ecb510f208b3e31e33734350e47748071f96416bf2086ec202c1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.9 MB (414900440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8580453fb6911287339ffd17ed807cedc699877a9750b9afd63881cd83d09c0a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Mon, 06 Oct 2025 22:13:31 GMT
SHELL [cmd /s /c]
# Mon, 06 Oct 2025 22:13:33 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 06 Oct 2025 22:13:34 GMT
USER ContainerAdministrator
# Mon, 06 Oct 2025 22:13:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 06 Oct 2025 22:13:46 GMT
USER ContainerUser
# Mon, 06 Oct 2025 22:13:46 GMT
ENV JAVA_VERSION=26-ea+18
# Mon, 06 Oct 2025 22:14:42 GMT
COPY dir:e6c654e75731597f0435b40aeddf616b12e3e120e9e2343d833678b37f3598da in C:\openjdk-26 
# Mon, 06 Oct 2025 22:14:51 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 06 Oct 2025 22:14:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b57cc4b440522859eb6ee57d0e0e1c8bd281b3354e9c16746f105992f1aa6`  
		Last Modified: Mon, 06 Oct 2025 22:15:22 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d467f2af8b135dc163bcd5d44e13c95e78b57b43ab26e1d2fa1c84b0ffcada3`  
		Last Modified: Mon, 06 Oct 2025 22:15:22 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d32c6ebd099e1619d23e924a5d3863ccf100474840190bfdda37c59e3786cb`  
		Last Modified: Mon, 06 Oct 2025 22:15:22 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8369d25322d7a357989c85b19f508c36821c227b16db38629776c1ac8ee16fa7`  
		Last Modified: Mon, 06 Oct 2025 22:15:21 GMT  
		Size: 69.4 KB (69354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef84c6d5ef33ad386269b17c5581869260f70e7054870491c013c1d39e8ded4`  
		Last Modified: Mon, 06 Oct 2025 22:15:21 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699045ff0f9205dd933b7ac608f280aeff8323b05b5c45d08cff720f014a6c83`  
		Last Modified: Mon, 06 Oct 2025 22:15:22 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1736b1809dea5973410ba96c301a05f0124029a8a9f9646f0a6d513b101366bd`  
		Last Modified: Tue, 07 Oct 2025 00:24:08 GMT  
		Size: 221.2 MB (221170238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e02b5c49f7786c3978a145c6b7e994a6e3f62430efe2d9c292bf3721609eeba`  
		Last Modified: Mon, 06 Oct 2025 22:15:22 GMT  
		Size: 103.6 KB (103588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bab902ec39106d0ea83345e48beb60e1a73c8e225c5a00528175809f291d11`  
		Last Modified: Mon, 06 Oct 2025 22:15:21 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
