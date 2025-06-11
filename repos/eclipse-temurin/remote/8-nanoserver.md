## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:801f6fd6ef2520b0f4f16e1865e80d0b813927e42837d1b17b7ffbf57e677f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:da2a759bec6d84620b3bbd309c1b63ac3f80c5f73815d14371bfd1eb1cae9859
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294720082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf92e68948830d8ff5fd2a4b30bcc98743640af6631abf1472f748ef3b21283`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:14:59 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:15:01 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Tue, 10 Jun 2025 22:15:03 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Jun 2025 22:15:05 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:15:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:15:12 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:15:19 GMT
COPY dir:5c4bbf817a67c787f7f2d8809dee99be16882c3512e063f4e47205ca5ccbd190 in C:\openjdk-8 
# Tue, 10 Jun 2025 22:15:27 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845b20b8c72caa2342a2d65d10a4a712c3c7037f606c861f93f6fe1762ae7e0a`  
		Last Modified: Tue, 10 Jun 2025 22:16:06 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a754945a78890c659dcea7a5aa331c2e38a78b887667dbb39c75c0881a1ab4`  
		Last Modified: Tue, 10 Jun 2025 22:16:06 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f789ca717edac3fb890a84c033af8f7590f152fb955278a1e3a7b6e3af12b8`  
		Last Modified: Tue, 10 Jun 2025 22:16:06 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1360b9eadc1025aaa21d4b751e244d89c1df1da9b3b77ded478ee72b67881d59`  
		Last Modified: Tue, 10 Jun 2025 22:16:06 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb57f4f797cef27168ede5a3862b9b1c67c9fae65d71144e9fc8f13d1b4e8fc`  
		Last Modified: Tue, 10 Jun 2025 22:16:07 GMT  
		Size: 78.0 KB (78035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf57366568a58c20bf13496e22753c1db5c6f093fbfc7ce65ea1be6e8a5b957`  
		Last Modified: Tue, 10 Jun 2025 22:16:07 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ba434edabbda39d25dd43b8ee1be46db3c4925dbe1bb9dea1e6910d77910f3`  
		Last Modified: Tue, 10 Jun 2025 22:16:19 GMT  
		Size: 102.4 MB (102440317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcce07ffc12fe8236011c903c62797c143ca83d3a3f811bd436ac77489df0646`  
		Last Modified: Tue, 10 Jun 2025 22:16:07 GMT  
		Size: 113.9 KB (113939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull eclipse-temurin@sha256:f1dc89ad35fba434ede6f005752eb5e5ddb2d1cb3196465eb00496c9542ec94e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225168198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51caedaf394d18b982c7cee0a5d855e6e0c768dabf3db7239fa48ad8ad9af80a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:12:42 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:12:43 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Tue, 10 Jun 2025 22:12:44 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Jun 2025 22:12:45 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:12:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:12:48 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:12:53 GMT
COPY dir:5c4bbf817a67c787f7f2d8809dee99be16882c3512e063f4e47205ca5ccbd190 in C:\openjdk-8 
# Tue, 10 Jun 2025 22:13:00 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed967f6f00e6f4d0334e98ee73290c60a08f95bee67f6e74a046c248455d5b0b`  
		Last Modified: Tue, 10 Jun 2025 22:13:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36d0f271249f256675395ec975096f65b9830e78970a5e3325d5646f95e923d`  
		Last Modified: Tue, 10 Jun 2025 22:13:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be640b77ac0a446245b6857332a08dae89d4159aaf3db8c0f81c595eb2ad9d87`  
		Last Modified: Tue, 10 Jun 2025 22:13:27 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfbd5d7a5aa8b95666aae21693e21b744ce15068b1286fa781c7d6eea87582e`  
		Last Modified: Tue, 10 Jun 2025 22:13:28 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897dbf363c0ee9dadca9cc9081cf7bb8237b4df6653c450662ba329d4b69017c`  
		Last Modified: Tue, 10 Jun 2025 22:13:29 GMT  
		Size: 76.9 KB (76924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82a452f70137cfb2385ca8ebb5261d94446252c75f90a0381ca2241f715e519`  
		Last Modified: Tue, 10 Jun 2025 22:13:28 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdbc66e838d16b9f7c387cf4867fb882f8b80195e356287ed8fe6ff609eac04b`  
		Last Modified: Tue, 10 Jun 2025 22:13:36 GMT  
		Size: 102.4 MB (102439279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0d8b000c58b5c313c246d90a19d914df089611d79c3f52e3b71ab9b780b134`  
		Last Modified: Tue, 10 Jun 2025 22:13:29 GMT  
		Size: 106.3 KB (106309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
