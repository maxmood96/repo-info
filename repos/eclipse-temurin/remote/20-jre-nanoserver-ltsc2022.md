## `eclipse-temurin:20-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:bed5b5aa0f45f37d34ffca0279af42eadc7cb672a1ef4e20bdbcee2ecaee6b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `eclipse-temurin:20-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:114a4c54a5112db61f0e810351d2e8d6074422178f388e7752daf704d3394a2b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166503525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1877fe71acc6015274616c69d3c4ed293775763e703f98bc3936861d37d00a37`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:11:36 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 00:15:21 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Thu, 10 Aug 2023 00:15:22 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 10 Aug 2023 00:15:23 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 00:15:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Aug 2023 00:15:32 GMT
USER ContainerUser
# Thu, 10 Aug 2023 00:16:16 GMT
COPY dir:7e69bb3960973ab39fc2ba0552343e70b32506a25a841e69600e9c49be1d11aa in C:\openjdk-20 
# Thu, 10 Aug 2023 00:16:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:ea9613880997b3ab2284a37c0c14a403553457b0c331b41c6bd6d1cc7838a222`  
		Last Modified: Tue, 08 Aug 2023 18:47:21 GMT  
		Size: 120.5 MB (120500677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3572ac06c9147f0946a40530f2197bb0101b82dd45b1defe04a8904a1c81a18`  
		Last Modified: Thu, 10 Aug 2023 00:30:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c858c43d3e6a9a3eff6b319404a1f9d4e8e209b3848f4ebe4844db5fe0a683`  
		Last Modified: Thu, 10 Aug 2023 00:33:12 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d07e124c511f04db80b6d58fd9332a9e6f0f6547d38cd19ea61f9d6555ff7`  
		Last Modified: Thu, 10 Aug 2023 00:33:12 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0274c2efbb42e692574088bbd3ca43b959d733d8c5466713050f9b0612ed0cac`  
		Last Modified: Thu, 10 Aug 2023 00:33:12 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959af0a666090aaf5f2e987624eb6b580fde01932e024dc30a16208a8010aa9f`  
		Last Modified: Thu, 10 Aug 2023 00:33:10 GMT  
		Size: 83.8 KB (83802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422f979be9d7f215d641f857cd4d38e61104c008a1487f17931f9c7f11977ecc`  
		Last Modified: Thu, 10 Aug 2023 00:33:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1db0147107ad48b83d5503831893a4288a60923992455bdf6be2fc2017ddea`  
		Last Modified: Thu, 10 Aug 2023 00:33:50 GMT  
		Size: 45.9 MB (45851633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b33c5b49f9baefa1568fa56c6805998d87f207655db8ed193c2b1f9c769563`  
		Last Modified: Thu, 10 Aug 2023 00:33:42 GMT  
		Size: 62.0 KB (62006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
