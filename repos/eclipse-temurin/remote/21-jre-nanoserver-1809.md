## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:a3869ce9b22092de45b3b607e5be0692fcc7bc2a35a22060bb5dfeaa065e59f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:254c95e70f5e34125637bfed5a3b4fcf9cf1adcbbdca3a6c18fcc509a795b139
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156781946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7667d5646562f3a6358254c08ae1f61de92cc2fb517e595d31dce8bb128e48`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 24 Jan 2024 21:53:05 GMT
COPY dir:a5c64f66204a1ce40e58093b44657f9abbd9eecac263988d919d778d3cf84131 in C:\openjdk-21 
# Wed, 24 Jan 2024 21:53:14 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:6784bbabef4c9b0b25ad98b0e405b7c4c8b4d154cc28590139759ebb7c010900`  
		Last Modified: Wed, 24 Jan 2024 22:11:12 GMT  
		Size: 48.7 MB (48749304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2eacba5fa6ddc4e1ac56a2dbefeb45a797cfadcef573f947e5bbe0e699dd12`  
		Last Modified: Wed, 24 Jan 2024 22:11:04 GMT  
		Size: 3.4 MB (3367301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
