## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:2f0beecbd471dafcd86b091b06999361dc100f6c28c456067af5ebbcab6a2aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:cd99a994a9edbcc5fbb5d1fec5f36f82b7d26b985eedbd13a19a47555fb659cb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.9 MB (394914240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751ed1009df585972eccd37e899e5ab77fffb5975f8dc75da6999c1638a9c283`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 19:34:35 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 19:34:35 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 22 Jan 2025 19:34:36 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 22 Jan 2025 19:34:36 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 19:34:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 22 Jan 2025 19:34:40 GMT
USER ContainerUser
# Wed, 22 Jan 2025 19:34:46 GMT
COPY dir:92a047b71eec51fdc82b01f518237bef64c78b39e065fcc3e9561b3909a60868 in C:\openjdk-11 
# Wed, 22 Jan 2025 19:34:52 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 22 Jan 2025 19:34:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025deb4acd18fe013bb7a99aa496a09e4a7fd186f5239655669d0a41a58f1e38`  
		Last Modified: Wed, 22 Jan 2025 19:34:57 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbc14cf4c9e6ad2c077406ab79b61b5fa8f7f3f458e54766ea5e93d910d2a04`  
		Last Modified: Wed, 22 Jan 2025 19:34:56 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832abaa20689d4524c047e3876a96854db8aad582b31077d3c777730a920bf96`  
		Last Modified: Wed, 22 Jan 2025 19:34:56 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1719de8f7bd72623fd85ac15cf75e58d73c41d59bf1314a962fb48582b6772`  
		Last Modified: Wed, 22 Jan 2025 19:34:56 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76df255a2ed981b14f005766e2fca791a18a8a54937c6d2ac84c824fd80fecad`  
		Last Modified: Wed, 22 Jan 2025 19:34:55 GMT  
		Size: 76.3 KB (76252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4f9390f0d6312d4cf9034855d97527b692c956804725df6dba8cf3f55ae8a7`  
		Last Modified: Wed, 22 Jan 2025 19:34:55 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebef3241164c48e8c3977f46353d0d9eef860df5330a9b57ac2439605c90d81`  
		Last Modified: Wed, 22 Jan 2025 19:35:05 GMT  
		Size: 195.7 MB (195673028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97796a264a7e6e42a51fc64185038a76ff78347b1a969014afae5b4b20db7f00`  
		Last Modified: Wed, 22 Jan 2025 19:34:55 GMT  
		Size: 104.3 KB (104320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4779daeb1dadd97090f52cd63869cff0cb7a9786121ec8e7f0a90f1e626023d1`  
		Last Modified: Wed, 22 Jan 2025 19:34:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
