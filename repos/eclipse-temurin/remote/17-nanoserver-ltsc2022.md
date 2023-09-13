## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8db4391ebe14ccf06e50c4f7b8374ff87f4b361d09a9eda2ac727b929a4fd2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull eclipse-temurin@sha256:75030e395d0d90758ea82a8ca40b0eb01ea0268285b7ed2fa1803f8cf6865eec
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306436493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3977d8395130041400bd2e3ee99d72604a23b951574a9d23e48313c1f0e46f1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Sep 2023 00:20:14 GMT
RUN Apply image 10.0.20348.1970
# Wed, 13 Sep 2023 03:28:54 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 03:31:14 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Wed, 13 Sep 2023 03:31:14 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Sep 2023 03:31:15 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 03:31:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 03:31:21 GMT
USER ContainerUser
# Wed, 13 Sep 2023 03:31:37 GMT
COPY dir:87d4868aeffb4665dc24a8514128e3f1a9351c7c90320c533fd29622fc9de6e2 in C:\openjdk-17 
# Wed, 13 Sep 2023 03:31:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 03:31:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f8cef0759210af9d01a2fb45d79956a2db738bbd3734b7244b17e14ad945cab`  
		Last Modified: Tue, 12 Sep 2023 18:47:39 GMT  
		Size: 120.6 MB (120567584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d67aef4c483590cefd40495efc212f13e4c62993e8036c20bb4e19bc8620508`  
		Last Modified: Wed, 13 Sep 2023 03:47:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8d421f21f43d0e258824a8327da02b26abed3d24883286056ab0d1719171dc`  
		Last Modified: Wed, 13 Sep 2023 03:48:34 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a5a6e6702b097d8587ecbb5f6abf31e9394317332fd48351918422f4ee2bb0`  
		Last Modified: Wed, 13 Sep 2023 03:48:34 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7d16f77e03c598328036fe852e884cfc812be8633393a34442fa909257b05f`  
		Last Modified: Wed, 13 Sep 2023 03:48:34 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a686e4257c37374cfc23e8b5698fc8cfe8f330e7cc6a27e9b532541367b4bba1`  
		Last Modified: Wed, 13 Sep 2023 03:48:32 GMT  
		Size: 75.6 KB (75626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec3c38f52d68a4afd9ca72b3a6ae47b3c16fa364025bce3f6d1da443518ee51`  
		Last Modified: Wed, 13 Sep 2023 03:48:32 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98aa999778f0b36b23e9772c360266d5b540410e3d65c7d3da7d72e060b5c004`  
		Last Modified: Wed, 13 Sep 2023 03:48:54 GMT  
		Size: 185.7 MB (185727025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d43234a694fbb421bf39434c2cf33ed661e4bfe916869351746c626701cadd`  
		Last Modified: Wed, 13 Sep 2023 03:48:32 GMT  
		Size: 59.7 KB (59693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e54efeef1be3bf4cb3bc780254957753ac43f131f09a3b597e280a498dd573`  
		Last Modified: Wed, 13 Sep 2023 03:48:32 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
