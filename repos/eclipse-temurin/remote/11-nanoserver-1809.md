## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f4b89b7691e2c6dbe626a8f8d23be93ceaa4a7bd6d08e39f2c099fd0b873e2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.3650; amd64

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
