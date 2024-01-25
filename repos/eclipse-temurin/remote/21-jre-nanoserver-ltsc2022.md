## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0b43edc5c5baf7dbe9fb3809351fa8a0185e9d33ec2e0ac14b43e8209a5431b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:dce5e2123347c372476a52d17aba7701ac4eb79ecd757d6a461cc9d12721f5c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169664156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f951922fc27cfaa721a204f7d743d4239f281540cc5015b512a940fd5220046d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 24 Jan 2024 21:58:17 GMT
COPY dir:a5c64f66204a1ce40e58093b44657f9abbd9eecac263988d919d778d3cf84131 in C:\openjdk-21 
# Wed, 24 Jan 2024 21:58:30 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:d82f480478ca72d97c4f69abc4a5673f8982ae6696a00d933a51bbf43d5da528`  
		Last Modified: Wed, 24 Jan 2024 22:14:13 GMT  
		Size: 48.7 MB (48749957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c96cd3e1b90083b28a072c82de1a8b431429108b6d23463cef5c79bd0444fda`  
		Last Modified: Wed, 24 Jan 2024 22:14:05 GMT  
		Size: 61.5 KB (61461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
