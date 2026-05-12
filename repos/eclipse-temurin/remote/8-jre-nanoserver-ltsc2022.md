## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d970dcd29cc666088b3bc82e0f071e80027be6a3845609efc9e47fd410e2b484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:548fdf994cc1a7d09afc9ad99e7afd86d581058122aa77b03a9aa2ebe9b7bbb8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167103526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465e994c2d7f365930a998a237eda47e57fb7e13aa03f1f3011623941b63f20a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 12 May 2026 22:09:20 GMT
SHELL [cmd /s /c]
# Tue, 12 May 2026 22:09:20 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 22:09:21 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 12 May 2026 22:09:21 GMT
USER ContainerAdministrator
# Tue, 12 May 2026 22:09:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 May 2026 22:09:33 GMT
USER ContainerUser
# Tue, 12 May 2026 22:10:39 GMT
COPY dir:deea9cd49fa78c2b910137007aed467626dd46389507789da1635093de3df40f in C:\openjdk-8 
# Tue, 12 May 2026 22:10:42 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef25a6bd0a5d088fd7d161f38a6fa9b306a38e4561457d556a3a61b32ca47fa`  
		Last Modified: Tue, 12 May 2026 22:10:03 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57fe2a0cb5c6bec4aacef0184e263f63388571a29a942d6dcfd0fc52a3bf481`  
		Last Modified: Tue, 12 May 2026 22:10:03 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3714022026eec71fe9060545f20ebea9d412d41f4c8892478e5eed5edc4ee7`  
		Last Modified: Tue, 12 May 2026 22:10:03 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f613aeef7e06ed751ec3858b8e274ea3ac03273e226122ec78f70679b7afd3`  
		Last Modified: Tue, 12 May 2026 22:10:01 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535e9b3adb43e9ee223b45aa1474371709a6dddb57f9d8c8bdcbc9de4d9853ee`  
		Last Modified: Tue, 12 May 2026 22:10:01 GMT  
		Size: 70.5 KB (70528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91807aeb1d0113c7e8cbc36cda06c2d4e01945e53bd7ccf6132619163b4cf67f`  
		Last Modified: Tue, 12 May 2026 22:10:01 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983a59f5db5315cf38392e7d93afe085eb90d74abfc5761ef635f64ecb9e4aab`  
		Last Modified: Tue, 12 May 2026 22:10:50 GMT  
		Size: 40.0 MB (39988120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac31f573e96e2b23f994b6d63eba7212d3b498a7d04d60b8a413e8d92f8978e`  
		Last Modified: Tue, 12 May 2026 22:10:46 GMT  
		Size: 83.6 KB (83627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
