## `eclipse-temurin:26_35-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:5df51191d037f22c45cbcf569e1b990ff8919d473754cb7fcd37cf6bd9188bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:26_35-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:d65f2a11f60e8efcce7329569bb86d2a7ed752de7b1d55c75ed73197392431ee
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187478186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b06ea3fe342a509ebfdf42b5d7997205ce1206898428c71b44b5aca02db1f8d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:39 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:25:34 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 13 May 2026 00:25:34 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 13 May 2026 00:25:34 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:25:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:25:36 GMT
USER ContainerUser
# Wed, 13 May 2026 00:25:41 GMT
COPY dir:45edd54e05e2fb7ffc611e6ef0c2df37aa13ac9c3c9a476003fc542e9ad17481 in C:\openjdk-26 
# Wed, 13 May 2026 00:25:43 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:bf24e90b95cdf703353e79847cddd8f95a9517ea6265fba8f3deb376278c8632`  
		Last Modified: Wed, 13 May 2026 00:25:49 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d06324963a3b92cad1a53bef36246288af6ba47a0567eb07dc3fd199bba31e8`  
		Last Modified: Wed, 13 May 2026 00:25:49 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01ec3af1282badfd5ee8199bdb976000db189f812fe577e08211dfc3c67e266`  
		Last Modified: Wed, 13 May 2026 00:25:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa237ae0ad2103e9a0b57d2cf12fd4b057fffb2584398b946eacf262f6aae78`  
		Last Modified: Wed, 13 May 2026 00:25:48 GMT  
		Size: 77.0 KB (77043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710f449f7dab7d21fd26a16b17d2a3d5435b8a22b1b1890d5d3c814891c27623`  
		Last Modified: Wed, 13 May 2026 00:25:48 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b646fdea65cbcb1109ed8dad6ac146d89968dbf98b14e75932b92fe8b2f85bf7`  
		Last Modified: Wed, 13 May 2026 00:25:56 GMT  
		Size: 60.3 MB (60266426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea0a3635a0a488aa29bed89f5b199022d91aebf391db1ada5d9187e868ef61`  
		Last Modified: Wed, 13 May 2026 00:25:48 GMT  
		Size: 90.7 KB (90675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
