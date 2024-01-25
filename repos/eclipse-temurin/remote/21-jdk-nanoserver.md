## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:31a6d66f0f90b8cfe78d8f613affe89f360948376008ad536f207b460df1c1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:f4ef98eb9e98b6494e7795b8ae384c4eb06ac07ee89c7c371f508824df2b1353
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322040895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f28d10d805d399ad3389a489fb5a95a3037985d659fb7e2fc24f11171f10eb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:57:24 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 24 Jan 2024 21:57:25 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 24 Jan 2024 21:57:26 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:57:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jan 2024 21:57:35 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:57:50 GMT
COPY dir:ef01cec12ba2d7ca328dd166c68dc318e8666a1382b059655285e6e080af62b8 in C:\openjdk-21 
# Wed, 24 Jan 2024 21:58:02 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Jan 2024 21:58:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5f2601f3a3b05b34c1f8683e3c9ea81ea63dbe1b04c37b85d09170f020fc0`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7821130a59cce22d4573c9f352600ba23c8f40966056a007db7f4c715da7768d`  
		Last Modified: Wed, 24 Jan 2024 22:13:36 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374b85dced44378a07bbb99342075dc176af11775f660f7e7c7662b404d5806d`  
		Last Modified: Wed, 24 Jan 2024 22:13:36 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2677c9064524c8dc67d5960709de339c5a00c1155c70d284a8f10378c5a45ca`  
		Last Modified: Wed, 24 Jan 2024 22:13:36 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b29b84d42f7c1bbf5de07951d6464345735d6831a9029124be0725ef93b16ab`  
		Last Modified: Wed, 24 Jan 2024 22:13:34 GMT  
		Size: 77.7 KB (77731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e75e6bd6effddc5f9e92f0264689d9b681ffccb91b4f448d0c29cba4fe08f3a`  
		Last Modified: Wed, 24 Jan 2024 22:13:34 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a5748b861a8daeba81b9e6f9a669404d0d2d9d61947da086f094509d5e686b`  
		Last Modified: Wed, 24 Jan 2024 22:13:52 GMT  
		Size: 201.1 MB (201125535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711227153180d302f67b4d6761f456ed9b9baba66dd1d3c6db110bfbb1bd349e`  
		Last Modified: Wed, 24 Jan 2024 22:13:34 GMT  
		Size: 61.5 KB (61491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77406bb521f74459f4ce8946f55e0d24d78e5d9c2317ab654064f5d9d0d8f221`  
		Last Modified: Wed, 24 Jan 2024 22:13:34 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:fbea5c2ecd94719047cd48870a44e60ba222b2149933b0e6f3df294b54abb53b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309610796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0523279e393812cee73c172b0cbec2682ba80d9c7f289971695e3061c2bc4c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 22:41:06 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:48:36 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 24 Jan 2024 21:48:36 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 24 Jan 2024 21:48:37 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:48:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jan 2024 21:48:46 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:49:00 GMT
COPY dir:ef01cec12ba2d7ca328dd166c68dc318e8666a1382b059655285e6e080af62b8 in C:\openjdk-21 
# Wed, 24 Jan 2024 21:49:13 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Jan 2024 21:49:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec88c6fd1d0cd14082069642ccb3b0dd5a7538a4b8b0c2d430549f345d8fd53`  
		Last Modified: Thu, 11 Jan 2024 04:09:21 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cec230829dbfcf404f6c33286166ea2078a19b9d68b0df812ecf36f024e6dea`  
		Last Modified: Wed, 24 Jan 2024 22:09:56 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a4733a1e7b5204caa5600e2eb27e416f65a832e6f45729f6a1ed8e163294bf`  
		Last Modified: Wed, 24 Jan 2024 22:09:55 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857afbd5749e10f14a05f80bf17299f68c74f57f74b6ef39324782790f49694e`  
		Last Modified: Wed, 24 Jan 2024 22:09:56 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971b4fd09ea068aef662c8791827450311f9b77d140c7c6510119a0c9b200a5a`  
		Last Modified: Wed, 24 Jan 2024 22:09:53 GMT  
		Size: 68.3 KB (68334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae59143b8d2d281ad288506d7bdcf851e63b207cdf90262d1e44c9c5e754b434`  
		Last Modified: Wed, 24 Jan 2024 22:09:53 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a014f06283402e136e0ded0afd2fb5edee12c3497cefb2faf0e3493eee0e1d`  
		Last Modified: Wed, 24 Jan 2024 22:10:11 GMT  
		Size: 201.1 MB (201125725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c8f39ff7608e3233798ceeba0d8104795389865fefd77e2a7968f230200391`  
		Last Modified: Wed, 24 Jan 2024 22:09:54 GMT  
		Size: 3.8 MB (3818553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe2772c5dce43e8229603f7ffb302a5486e4fdb66d804646ab434651424830`  
		Last Modified: Wed, 24 Jan 2024 22:09:54 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
