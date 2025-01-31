## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1881c2cefc535dfc48c61f3f99b9e05348db23ef3029e745edbfe19739e9a1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:bbeb4b16b2e5030fee82ccd1aa18c531ac5a4a24e6abe4d79851fd075b3c1f87
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164505794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6c45b217c54b3f4621993babfad1083de5070d71266224547bf7518bdf5c02`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Fri, 31 Jan 2025 02:11:27 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:27 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 02:11:28 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 31 Jan 2025 02:11:28 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:11:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:11:48 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:11:52 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Fri, 31 Jan 2025 02:11:57 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18740068f2dd25ad338d37afdf7ecf4b89f9e0c57941a3d9fa2adff9831377c6`  
		Last Modified: Fri, 31 Jan 2025 02:12:00 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695acdfe86a31d9f59f55c038a808e87a5f039991e086ac683fb86242ccce4a7`  
		Last Modified: Fri, 31 Jan 2025 02:12:00 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7655994ce5ca894acbc945990b19895665df2f717b7df9ad2bed5dd77f3abaa7`  
		Last Modified: Fri, 31 Jan 2025 02:12:00 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a19d4dd4c6ce426d5c32f1a5af1d5659b738ded8e4f4adf9c4de5437a2ad58e`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7134024a8b126c7d382b9e29dea0b0ca18cff360e8d423e9b0b572bc88608a6f`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 87.8 KB (87793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c1925a5bbf9e11a9fe4c5b76425799c3eb9f582f5f81bfe11a602b8f3d860d`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5711b3bab6634d8ec58dc48df4a20cbf86683110f444fd7f0ac69d25403f45a8`  
		Last Modified: Fri, 31 Jan 2025 02:12:03 GMT  
		Size: 43.7 MB (43654567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1697c5e6bc1d709ba2dde5c4f9da01b1e59a74e6331bd54711944b998b18aa5`  
		Last Modified: Fri, 31 Jan 2025 02:11:59 GMT  
		Size: 96.7 KB (96732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
