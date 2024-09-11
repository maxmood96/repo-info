## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7082439300eb469a9992ecf97a6c258657de6432cb19a4fcd8826227baeae0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:d13c6a2e2b161bcf35c03f12450c11174dc0d3e25595684bb670dbfb47b6f950
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164002238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46280822cbcdc466d3a5388f03bc030fef7c14da0035573b51446cf1a7f45b7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 01:05:47 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 01:07:59 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 11 Sep 2024 01:08:00 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 11 Sep 2024 01:08:00 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 01:08:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 01:08:09 GMT
USER ContainerUser
# Wed, 11 Sep 2024 01:08:49 GMT
COPY dir:4243678b5415f703b690863e65df7851d84efb271bd792cb5cbd95ab7bb17263 in C:\openjdk-17 
# Wed, 11 Sep 2024 01:08:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f530aeae2fa9f5c34641a19099e9949880479ad7319678bd0506ba1927a95`  
		Last Modified: Wed, 11 Sep 2024 01:33:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3021472a8e25674fd1e2edaffc9035ecc67f7fff59688db85cb268ac0bf1c0d7`  
		Last Modified: Wed, 11 Sep 2024 01:34:36 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bbb0629480851b9c01ab54847fe0fd454a054dbed8c2737492fc9b837e84c2`  
		Last Modified: Wed, 11 Sep 2024 01:34:36 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39578ebc4c5f739baa00595b756d93ca29d27a7bd955082e767d6d8b39a9df77`  
		Last Modified: Wed, 11 Sep 2024 01:34:36 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b37c4887ed0e155262e27bba83e5297d7c1be1e3b033c75ca59680a919d813`  
		Last Modified: Wed, 11 Sep 2024 01:34:34 GMT  
		Size: 76.2 KB (76193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ca761024e3880368ef22acc0dbb413cfd6402fbeaed7165730f565b0465112`  
		Last Modified: Wed, 11 Sep 2024 01:34:34 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8f3ca93f382f33632ce8b8fe50e0f70e266363d08207a5e3ca1de280377114`  
		Last Modified: Wed, 11 Sep 2024 01:35:08 GMT  
		Size: 43.3 MB (43349280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fa2bd161f6419e2c95c6f54c38e39882196e1ca9e2b82e4e043816921ca322`  
		Last Modified: Wed, 11 Sep 2024 01:35:01 GMT  
		Size: 61.5 KB (61540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:79aca653b0b920027b95dd525005ec530f6a1b2ca28b7c6c69782edf18fec9b2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 MB (201492501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988e2d43b5b12dd4e422d34f67bced00b765c1aa25c663b9c105d6269906b53e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:38:01 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 00:50:23 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 11 Sep 2024 00:50:24 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 11 Sep 2024 00:50:25 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 00:50:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 00:50:33 GMT
USER ContainerUser
# Wed, 11 Sep 2024 00:53:17 GMT
COPY dir:4243678b5415f703b690863e65df7851d84efb271bd792cb5cbd95ab7bb17263 in C:\openjdk-17 
# Wed, 11 Sep 2024 00:53:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340318059288cbbdb326eea5b7079e789361251409038a37867d4e395c9404a5`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91950d63fc5ef50eff89ea5d9b367978ab15d1e8be06ea71699f45ef2aa3fd09`  
		Last Modified: Wed, 11 Sep 2024 01:26:28 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f5a9c07212454d0e55d94a8bf0c20857e04ea2239ce45e54b6dc2e3427b2e6`  
		Last Modified: Wed, 11 Sep 2024 01:26:28 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec22c9c1b01867beec0be83f2b95feecea9d4d3f8eb581673baf3b5a462ae553`  
		Last Modified: Wed, 11 Sep 2024 01:26:28 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099df04b57eb6987eb23da28ae2dc75eb6f0e9237082b3d2c99cf620b7304c02`  
		Last Modified: Wed, 11 Sep 2024 01:26:27 GMT  
		Size: 67.5 KB (67532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a75f0f06fa9dfcf8547164899e5cf4c6ac8a7ac73e9a4a149b98dbb15febe9`  
		Last Modified: Wed, 11 Sep 2024 01:26:26 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435c098e2c1b9fe79ab760abd40e9d01394004af15c379594c7807b908fcc6c3`  
		Last Modified: Wed, 11 Sep 2024 01:27:37 GMT  
		Size: 43.4 MB (43357562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a4465a4e4c578da156d674d0dcfe0ac6ba29cc986e31463620d1947453e3c5`  
		Last Modified: Wed, 11 Sep 2024 01:27:31 GMT  
		Size: 3.0 MB (2980820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
