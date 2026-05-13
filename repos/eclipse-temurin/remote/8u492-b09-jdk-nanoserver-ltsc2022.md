## `eclipse-temurin:8u492-b09-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:f160dc7a7e04385af85e440350d7e5f90012956f12909573a40e1a7aff1b7afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:8u492-b09-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:da7e484904ba251f66a9dbea251c4757df1e336379d86d65683780187965002a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229137812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcbef4f687640db10b0557baba3e2afc1866ba782f6175a69fdc4aac577ab87`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:39 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:23:39 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Wed, 13 May 2026 00:23:39 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 May 2026 00:23:39 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:23:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:23:42 GMT
USER ContainerUser
# Wed, 13 May 2026 00:23:47 GMT
COPY dir:25077d8770e7edce418eff57fe3a0561246eac55d5c42b7efa90e67ec851bbed in C:\openjdk-8 
# Wed, 13 May 2026 00:23:51 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60ed370d326231e88b53b9eb83b5e7c2a02f147b495f0751da4e9072d5d7a91`  
		Last Modified: Wed, 13 May 2026 00:23:57 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050aab815d610a4bd48b5a653d122941131b01feda5417d9688a0f3b82272cdf`  
		Last Modified: Wed, 13 May 2026 00:23:56 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f22fcf9e1d7c0a19ea09aab98495f547377556c83c169c85e4c12fad52e316`  
		Last Modified: Wed, 13 May 2026 00:23:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc2c1c53a66405d56f5da343a146fb64c1978069466b3add8ed6f894fc005af`  
		Last Modified: Wed, 13 May 2026 00:23:55 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ad2120606fcb1dc08af46834b6cd1f28df74cd10fa0d07f99566b2dc33e2e3`  
		Last Modified: Wed, 13 May 2026 00:23:55 GMT  
		Size: 77.0 KB (77035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5b9d8f7ca6a43f9c1a93f7979cc4e5178030dce253001b8d38723b7a8e6a89`  
		Last Modified: Wed, 13 May 2026 00:23:55 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a0241be7f0e8fb03a01eae41e06176789dd3be5926718fe433781c6bdc5db9`  
		Last Modified: Wed, 13 May 2026 00:24:03 GMT  
		Size: 101.9 MB (101915733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2ac86b2533b6d0afe82141558721f824a41c6ec443f62e5a83813b68935bfe`  
		Last Modified: Wed, 13 May 2026 00:23:55 GMT  
		Size: 100.9 KB (100936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
