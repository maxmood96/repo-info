## `eclipse-temurin:21-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:dcbc72b05aa71d9aa4c2b777fc3d68a7a6ee314fb4263859302bc3502e387842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:5abc5c45958d3c47ebce685f95244766e9ed5be428ac80b5b251a3ecb7f7b5eb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.9 MB (328895244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb98902f472b5aca80716e696e7455f655ace374f384449cf700a95c41c8bd5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:12:13 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:12:13 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 14 Apr 2026 22:12:14 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 14 Apr 2026 22:12:14 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:12:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:12:17 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:12:49 GMT
COPY dir:a00a0ee8f4ae82aa8e2b5d2b9cb5c2941887de3e7b021ae64d7924c257e6915c in C:\openjdk-21 
# Tue, 14 Apr 2026 22:12:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 14 Apr 2026 22:12:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f00710bba7cbe6555960ffb1a4f2ca8364d191d9c6666e21e6080e462bd9d0d`  
		Last Modified: Tue, 14 Apr 2026 22:13:01 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678739d69283d7f6dc16fa46a0b29d06f901611d711454a65636ddeddd47436c`  
		Last Modified: Tue, 14 Apr 2026 22:13:01 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098a7b61e4275f71f19efda8fa76b9aad9a55c3d6c06868446dbde626fc0d876`  
		Last Modified: Tue, 14 Apr 2026 22:13:01 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b98f44e6adf62e2789c599893f1799bd759adddfc851b66929bb51fac5acf8`  
		Last Modified: Tue, 14 Apr 2026 22:13:01 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83d3728a601f60db1cbf7ecf6124f4383182fe0f27f1c092a39051b6ef9f3a4`  
		Last Modified: Tue, 14 Apr 2026 22:12:59 GMT  
		Size: 72.6 KB (72581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fe3ef67fe5119a6701674b7d048940759295761c6520ca11059fae12d34bc0`  
		Last Modified: Tue, 14 Apr 2026 22:12:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd43cb954c4037f059203d754a485e2805418e7a5e36f4f882b71c9285b8b23`  
		Last Modified: Tue, 14 Apr 2026 22:13:12 GMT  
		Size: 201.8 MB (201752439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d04da806f2dbc97e049c3991fbc8d2332ded1cfd3ffaab0b4055f64184309f`  
		Last Modified: Tue, 14 Apr 2026 22:12:59 GMT  
		Size: 107.9 KB (107886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7ec614eddc84c79d456519f48d3d5214de07327574adc9192bceca8e6a0c5d`  
		Last Modified: Tue, 14 Apr 2026 22:12:59 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
