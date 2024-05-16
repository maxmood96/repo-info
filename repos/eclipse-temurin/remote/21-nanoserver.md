## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:5df933dcce3df59a18d23e4c47622f0b987846b1b3b5305e420836a5a5bd67c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.2461; amd64

```console
$ docker pull eclipse-temurin@sha256:4119faea8e4a0e88b15cde5cccaff77aa2473b17161d9ba7d7d6a9580ea62f4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321716605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb40c8d629d7e64af63287073ce907bfe56fd36c664db2a14612759e9e4248c5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Wed, 15 May 2024 20:32:41 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:36:55 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 15 May 2024 20:36:55 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 May 2024 20:36:56 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:37:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:37:06 GMT
USER ContainerUser
# Wed, 15 May 2024 20:37:20 GMT
COPY dir:23b4ead9c2036754f644b00182bded9da6af0a8e5b9adaf18f46a103fb435a07 in C:\openjdk-21 
# Wed, 15 May 2024 20:37:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 May 2024 20:37:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5560c76ac3d9aa2d8a6dbf79d443a7e1d170aae31c940cf791c9b532d5756a1`  
		Last Modified: Wed, 15 May 2024 20:58:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda6608870fce2c13c86ab91e9f607b9862d3c548045bee576d9baefd3d22f7c`  
		Last Modified: Wed, 15 May 2024 21:00:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0518617a8ea970e9e5195ac41a01ca64cf3a72c2e847651581d470838aeeb2e8`  
		Last Modified: Wed, 15 May 2024 21:00:28 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d665857a6bb1e36593f7c70701084ce53ef295002e87e14ff06eefa459da285`  
		Last Modified: Wed, 15 May 2024 21:00:28 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233c65ea3e60064f4860406b1ebdc9e6f0a9c673c0088e35e7a4976263dff606`  
		Last Modified: Wed, 15 May 2024 21:00:26 GMT  
		Size: 74.3 KB (74347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c280ad1b4f912c4574466274c8fad293d115b0e3abc25ca4e3e87d41a41918`  
		Last Modified: Wed, 15 May 2024 21:00:26 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78759b2241b363745926a004cc6c512c4ab78cc860b296260d8f5778217bd145`  
		Last Modified: Wed, 15 May 2024 21:00:45 GMT  
		Size: 201.1 MB (201148237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573ca166dd87b4d0fac962b0fb95e5b7b864848b05eee1be48dbdaa900ccac82`  
		Last Modified: Wed, 15 May 2024 21:00:26 GMT  
		Size: 61.7 KB (61723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aa75633a8f2c99ddeee1cc8492901bdca3414d4ac6953c3b6c9e676a098936`  
		Last Modified: Wed, 15 May 2024 21:00:26 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:03aeae94a22b6e0b27e6b6f42f84d6b5094d1169698def0d76568fd1879e04c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.0 MB (359980691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e651e026ad4453b6a9b411cbbbd5ab7f64b344ee3e15838f17c29568e4cbaf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 19:42:01 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:15:47 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 15 May 2024 20:15:47 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 May 2024 20:15:48 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:15:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:15:59 GMT
USER ContainerUser
# Wed, 15 May 2024 20:16:17 GMT
COPY dir:23b4ead9c2036754f644b00182bded9da6af0a8e5b9adaf18f46a103fb435a07 in C:\openjdk-21 
# Wed, 15 May 2024 20:16:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 May 2024 20:16:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6a511fea8e874efc08e5058ac5b12b6433c36ba6570862a619dd80cfb0e190`  
		Last Modified: Wed, 15 May 2024 20:45:52 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4841491247350a2cba22e1d7deecfc13e43a405a6bf7b96689d0b169bf4a4fe0`  
		Last Modified: Wed, 15 May 2024 20:53:51 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a6273893979eaf90f1cf0ba4b42c4c9369bf97d556f2e62ba9fa4eff08f910`  
		Last Modified: Wed, 15 May 2024 20:53:51 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c33ee8b266be6936b2f35575cf3a5a5383bee76bbe81975578e99f6651514d`  
		Last Modified: Wed, 15 May 2024 20:53:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d775a9c260301bb3c11962dba072c4a531ef28a1f85dc32dd705e3e05daad8e`  
		Last Modified: Wed, 15 May 2024 20:53:49 GMT  
		Size: 68.4 KB (68439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18782632469d51a768f172daa64d27fc8cca50a0276127a4c4f5ef26e28973fb`  
		Last Modified: Wed, 15 May 2024 20:53:49 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597db69c94367a5058f268265337e52e14d52dbe49f6444eb6310f9b062de27f`  
		Last Modified: Wed, 15 May 2024 20:54:08 GMT  
		Size: 201.1 MB (201147743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96666d60f4890b69fe1cbda68f88ca4aa5ee89d90505905ab1274f34700c1fc6`  
		Last Modified: Wed, 15 May 2024 20:53:50 GMT  
		Size: 3.8 MB (3816668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c6d6e7546e5d13be27a18c32509f449b54d1dca8692ef0cf01e95d7faafa2b`  
		Last Modified: Wed, 15 May 2024 20:53:49 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
