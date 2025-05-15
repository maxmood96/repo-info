## `eclipse-temurin:8u452-b09-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:10a57b8ba13a01abe37dede080607efa43d76dcee7a946d28fc18e45396871e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:8u452-b09-jre-nanoserver` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:9ef36eb7e5bbf6db869acec8997b54a89ebb1df73e63c41031310abecdc2bb5c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232139921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459d66c109279818beb4035bd0bce40b073c7ade1905a62bea0cb94b526397c3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:13:56 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:13:56 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 14 May 2025 21:13:57 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 May 2025 21:13:58 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:14:01 GMT
USER ContainerUser
# Wed, 14 May 2025 21:14:05 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Wed, 14 May 2025 21:14:09 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587d3f7a31a00daa3d8037b092c45f12dff1c4e2211dfa1e0ad27e8cfedae988`  
		Last Modified: Wed, 14 May 2025 21:14:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528fda69d46c0888df8776440197e14f799e46aa65ab1a67a81ca44294ca195`  
		Last Modified: Wed, 14 May 2025 21:14:12 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f897a8210cf92030cd3b7298c7f5204e052d91f72b0d05620173cfa23d42ec0`  
		Last Modified: Wed, 14 May 2025 21:14:12 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f0fe9d4683283742285c4e04b8cfc1a4cf559628b076211aba0eb4ed998b9f`  
		Last Modified: Wed, 14 May 2025 21:14:11 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8904ade50e251bb53d65dd17c8e14fbb18eb85c9f72a5705ddd2ef0250f5462c`  
		Last Modified: Wed, 14 May 2025 21:14:11 GMT  
		Size: 76.0 KB (76025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdd5ba619b6852abea2b2a1e124b42fd20d0d6d0bebe7eef2f468911f451a6a`  
		Last Modified: Wed, 14 May 2025 21:14:11 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef624b7a572b9dec09c4cedb0ea6101128e81a207609c73b22694f26f648590`  
		Last Modified: Wed, 14 May 2025 21:14:14 GMT  
		Size: 40.6 MB (40554076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7670a666c46450e23e17ae52584bdaed27ab5cb21fc9cc412c6d1549b02d423`  
		Last Modified: Wed, 14 May 2025 21:14:12 GMT  
		Size: 92.5 KB (92479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u452-b09-jre-nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:930484efb6e2b3ee9f42584da90672f55c73d88ded79df6b3f1566a4c9440f30
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163308493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f2da037dbde7e96982dc056f396e6f67593ca8d695e87faf2d7ec2b9bc7f5d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:12:13 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:12:14 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 14 May 2025 21:12:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 May 2025 21:12:15 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:12:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:12:18 GMT
USER ContainerUser
# Wed, 14 May 2025 21:12:21 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Wed, 14 May 2025 21:12:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ae651cc91f06b415e55640e4dc7b07bd999822210663d662a0ec9043c5d391`  
		Last Modified: Wed, 14 May 2025 21:12:31 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66a7765f157e34c443a8af0df411f21f6904b3e22ae841446215727bbba8892`  
		Last Modified: Wed, 14 May 2025 21:12:31 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6476bb55afc8227cfc5081d2573d12d55fa4ffadb183de589b119911e9926c9c`  
		Last Modified: Wed, 14 May 2025 21:12:30 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aecdc18d31f3aa91dc7a0905eeb4d4cde31da2ecc611d1f9b4cbda821a3c5e9`  
		Last Modified: Wed, 14 May 2025 21:12:29 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719f2cc2f8ebfddc68ecab79ad4799c4b9090cc087ab8cbcacafd7c480019eff`  
		Last Modified: Wed, 14 May 2025 21:12:29 GMT  
		Size: 76.4 KB (76352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28906281c141570e3a0e85ccadd76d1e62a0b750bf269443a9f2fa768a366e3`  
		Last Modified: Wed, 14 May 2025 21:12:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f98cc9ff146c88853184973352bd0cf68cc9d0bbb3d622dfbaba7857317fba5`  
		Last Modified: Wed, 14 May 2025 21:12:32 GMT  
		Size: 40.6 MB (40552739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1df2202a7285227d2bbaadf1bc9292346e7ea53ac024b33da68bb505914def`  
		Last Modified: Wed, 14 May 2025 21:12:29 GMT  
		Size: 97.6 KB (97627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
