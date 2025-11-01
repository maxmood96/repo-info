## `openjdk:26-nanoserver`

```console
$ docker pull openjdk@sha256:1b2ebba450edc3ff90f8244d8a7cadf6f2870a6b99534e28051bfe0d7bf23f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:b2de8d70afa2dd3072077ceb7941c379dc161d000aa12ba9c858d463b1f38b83
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415494548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd168944a22f4e97a234b780660702effd2ef8821e768774cf2b7bd00a9bf037`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 31 Oct 2025 21:15:15 GMT
SHELL [cmd /s /c]
# Fri, 31 Oct 2025 21:15:17 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 31 Oct 2025 21:15:18 GMT
USER ContainerAdministrator
# Fri, 31 Oct 2025 21:15:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 31 Oct 2025 21:15:33 GMT
USER ContainerUser
# Fri, 31 Oct 2025 21:15:33 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 21:17:01 GMT
COPY dir:c90d7d97d7a92e44aebce14c599d37116856dad8a1bf4d9fcb77de537cf1c0aa in C:\openjdk-26 
# Fri, 31 Oct 2025 21:17:10 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 31 Oct 2025 21:17:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058a353c2488f5ee182f90c36c5f683339a76ef6dca6089ad1d58e10e593bc2f`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2e48dfa4158c36bb6d22ea93a894cc958d7c0de9fb0cbe376e13623362cfe8`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574756a6681a7e7509dd222da5c8270e4263624a80ab28426f8b8ba042d6aff0`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b191ad5485c6707a4dd219f060de3fb5dad14366bb7025e461dc6b466762b8b2`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 71.0 KB (70972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72ee8ba120d678ddddd8e0704d914eb728a9646d1aac3164f08060fc28ebda3`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0bcdd1b4d84adf65b7c3ba5af7af01b02310230018db10a7f1acc0ea5bddca`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0f3d24fadbd551bf8e484526826d62a9f67014fa431c962d90cac6a80f310`  
		Last Modified: Sat, 01 Nov 2025 00:23:55 GMT  
		Size: 221.3 MB (221284997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02213e244532eccaab7bbf907ee0f60c2ffc4923bf5278f21b85ada58c34c0a`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 102.8 KB (102758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d8be3c61cc2e4585ee47dca34bf7291c7029ae649779e1134285c52a12e71c`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-nanoserver` - windows version 10.0.20348.4297; amd64

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
