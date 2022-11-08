## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:5773821267e65bd8113ad22f495e24a593fef82bbb52260bfa14d0ec3fb30ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:3d0b8c4a5395e2dc9384264d0393bb5479e7dffdfae6eb5a4f92679046580295
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314772628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecb14384faa6abd8812ac7b946da0fec99a1f8b4d071abb87dfd2bb5c4dd212`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 07:21:30 GMT
RUN Apply image 10.0.20348.1249
# Tue, 08 Nov 2022 19:27:23 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 19:29:25 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 08 Nov 2022 19:29:26 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 08 Nov 2022 19:29:27 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 19:29:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 19:29:40 GMT
USER ContainerUser
# Tue, 08 Nov 2022 19:29:58 GMT
COPY dir:cba9eceeddb80383417f5e5518328c343fc4183981a343fca253ea7c2e4dfda5 in C:\openjdk-11 
# Tue, 08 Nov 2022 19:30:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Nov 2022 19:30:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72e5d750fe8c1a32d4a26ef3b4a4e1f6124ac079b142f12724af2abfcba1c8b3`  
		Last Modified: Tue, 08 Nov 2022 19:57:58 GMT  
		Size: 122.1 MB (122092167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd83067a7e6c6d9dab3ac0265a21919de95a0bf4e737e647fbf3e43c9874b0`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf64ef5841c3055c97da30afe94e91f36d8258ef461b52540da9903c4e3bc9a`  
		Last Modified: Tue, 08 Nov 2022 19:58:33 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c375a4f91fe23421131785b0b42e01c977a392cf2b3e31402bf0d22f9485b2`  
		Last Modified: Tue, 08 Nov 2022 19:58:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37f60d8c806f3324c10a3f609dd590835d2f256a88a14d5555cbee6050df6e4`  
		Last Modified: Tue, 08 Nov 2022 19:58:32 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea17a3ec8151119077e9676e7507f58607330aade351454cc2b611ce183fdc90`  
		Last Modified: Tue, 08 Nov 2022 19:58:30 GMT  
		Size: 85.1 KB (85094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d30911c1c2bad5db46115e443e5a3fb3242f0d01dae68a8b470990aee8b83c`  
		Last Modified: Tue, 08 Nov 2022 19:58:30 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99d50bef7a099fe6463304b115c4b24172dac9bec424c286ad03ec798cd562b`  
		Last Modified: Tue, 08 Nov 2022 19:58:51 GMT  
		Size: 192.5 MB (192525543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785564f2b554d5b86b2eaeaea535fcc4d4f041c73321ad3988209f5a1ef2ff60`  
		Last Modified: Tue, 08 Nov 2022 19:58:30 GMT  
		Size: 63.0 KB (63035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274fb86a4f00c053ca29c6dd7db990ee5829915e5bd225df86168f7fe269fea7`  
		Last Modified: Tue, 08 Nov 2022 19:58:30 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull eclipse-temurin@sha256:cc11354a7cd128caf3f594c5d25f463866bb5336dd155405235acd24c78bbe50
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299407772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc7ec5dbc1f11f402375cd4ea3c914f9cc19a99c126226be72d98ce201d0a00`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Tue, 08 Nov 2022 18:36:25 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 18:51:15 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 08 Nov 2022 18:51:16 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 08 Nov 2022 18:51:17 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 18:51:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 18:51:34 GMT
USER ContainerUser
# Tue, 08 Nov 2022 18:51:51 GMT
COPY dir:cba9eceeddb80383417f5e5518328c343fc4183981a343fca253ea7c2e4dfda5 in C:\openjdk-11 
# Tue, 08 Nov 2022 18:52:14 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Nov 2022 18:52:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e8f4bb4b79b67857c1e4ac5c66026fd5ff5badbde5a8b59b11251b02699586`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e31d7a079d8015c583b6bf92d9578552be10348f6e39dfdfc7fcd3f0709288d`  
		Last Modified: Tue, 08 Nov 2022 19:48:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7057989690fc8ef5f9b0a864b96a374e3085973d23e6a890d4cd9dceb8868c9`  
		Last Modified: Tue, 08 Nov 2022 19:48:08 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36298ec2e53419f44640e53a23afb93709de306ebf9acb2ce5abc232a12a76e`  
		Last Modified: Tue, 08 Nov 2022 19:48:07 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c19e765a35428811d9125073672b2bd1d30252c50e959f9e177eff49496977`  
		Last Modified: Tue, 08 Nov 2022 19:48:05 GMT  
		Size: 71.2 KB (71191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22f76bb3259773dd98831017ffddef9fc9764e384de52bfc050fa7bfc098bad`  
		Last Modified: Tue, 08 Nov 2022 19:48:05 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86827ba219bfdabef64d60d13751fc3b5bed3bd7727b79c4261a66f369c6d6a`  
		Last Modified: Tue, 08 Nov 2022 19:48:27 GMT  
		Size: 192.5 MB (192523732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef78fe5b1068af442c640197c44c81b186a2d9a9a4d202b8d011f9722fc8bd29`  
		Last Modified: Tue, 08 Nov 2022 19:48:05 GMT  
		Size: 82.5 KB (82510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4966b0498b100510f407cfb09a7049b44cb19af6cb54c6aab7dc6f0492c1d50`  
		Last Modified: Tue, 08 Nov 2022 19:48:05 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
