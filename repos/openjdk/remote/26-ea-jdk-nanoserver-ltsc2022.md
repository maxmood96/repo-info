## `openjdk:26-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:d1cdb3b2c5fbca7325d41898d1c59a419a840d9f5339bde47c52cdb5fe13cd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull openjdk@sha256:7e76bd8f26e5401a53e14c952dcfa649e6cd21c1fe115ba959e536ba3a32b886
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.2 MB (344186815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a41c32d7781a1f33f7cdbb8e5abced8c03ab3d7255f87b3467f2fba959dc2a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 31 Oct 2025 21:15:07 GMT
SHELL [cmd /s /c]
# Fri, 31 Oct 2025 21:15:08 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 31 Oct 2025 21:15:10 GMT
USER ContainerAdministrator
# Fri, 31 Oct 2025 21:15:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 31 Oct 2025 21:15:26 GMT
USER ContainerUser
# Fri, 31 Oct 2025 21:15:26 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 21:16:28 GMT
COPY dir:c90d7d97d7a92e44aebce14c599d37116856dad8a1bf4d9fcb77de537cf1c0aa in C:\openjdk-26 
# Fri, 31 Oct 2025 21:16:37 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 31 Oct 2025 21:16:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26663b52bd6c99bef6ebfdc2cc76691beb554dd529b088bbf48a68ebd5cf09c0`  
		Last Modified: Fri, 31 Oct 2025 21:17:10 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9060d7fb3056f3f4b5ed6c764a00267c5887deea5e65f099da670977a7f8209e`  
		Last Modified: Fri, 31 Oct 2025 21:17:10 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1099066d29796907b25c3b7324dd4514804266f329b07829fe3305fa58c494`  
		Last Modified: Fri, 31 Oct 2025 21:17:10 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fdbcfd5385ba02e3a962907a481f127f8147b73c8ce75d14d2a17f3100caef`  
		Last Modified: Fri, 31 Oct 2025 21:17:10 GMT  
		Size: 80.4 KB (80426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4dce7ffdd851b20af21ea3de7c1b008c73973eec4fcb411fdc1cbe1990d9d3`  
		Last Modified: Fri, 31 Oct 2025 21:17:10 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a27cf43e3468e9d226298bdb5cafef97ba26c02e023a524fcf0e01471daf5ae`  
		Last Modified: Fri, 31 Oct 2025 21:17:10 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278216870dea3e66ae3c40a9adf8c471db8a391092fcdfcab3bfef245411bac3`  
		Last Modified: Sat, 01 Nov 2025 00:25:30 GMT  
		Size: 221.3 MB (221284702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7099ce2e0d4aafc36b5f274ce69db3863e446a38979a49cb86d6f1718273ef`  
		Last Modified: Fri, 31 Oct 2025 21:17:10 GMT  
		Size: 131.2 KB (131215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ae603378158b78e7ea94f9abd724b86e10bdc32297d5ca5b697aef6b7ac029`  
		Last Modified: Fri, 31 Oct 2025 21:17:10 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
