## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:abb2c0b9a2469c26d8cabacc7c4dabbebfb41fd27ef2206884771882a91c401a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:438f4ba58f04e0220089b281d311bc2b50f9199e7ae928e190177a1affcb84e0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223281047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80c005a6500f9f98ea98d47c10c31d312606f8e0a779680d128d35d24c5f5f3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Fri, 31 Jan 2025 02:11:02 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:03 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 02:11:03 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 31 Jan 2025 02:11:04 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:11:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:11:09 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:11:14 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Fri, 31 Jan 2025 02:11:18 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Wed, 15 Jan 2025 01:24:28 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f199657438eb77d59b38021b80b14f2ba6015665359c6a0afa05c2e205bed57`  
		Last Modified: Wed, 12 Feb 2025 23:32:57 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ea1a55f99aefad6f39abb828497624366e3433865d9f23c9dbc72c326e5ec5`  
		Last Modified: Wed, 12 Feb 2025 23:32:57 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907a90a47bc784357b6b98b0758b9b7d5e76ed5b286421afb35472d697e51d70`  
		Last Modified: Wed, 12 Feb 2025 23:32:57 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f03657d108ee9d764cae4730ba77e610878f96af0f352512c8863afcb7cfa5c`  
		Last Modified: Wed, 12 Feb 2025 23:32:58 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fec1f9ed5adb9cdbcc25c921412c89c57d3ad3e144125957a83169e0c1e384`  
		Last Modified: Wed, 12 Feb 2025 23:32:58 GMT  
		Size: 73.9 KB (73866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4ca3b437598b503811c258714e84a98506222eab0b9857f57d9b1e56e2cd1f`  
		Last Modified: Wed, 12 Feb 2025 23:32:58 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d8df7341554e72cee8cb1ea3dd0eabe94546ed4d6b05999eb2ca849b4e4b4f`  
		Last Modified: Wed, 12 Feb 2025 23:33:12 GMT  
		Size: 102.4 MB (102431296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b590648c85ada435b0bc54e291b110cc840685700d3703b212a5fe3102cb4b32`  
		Last Modified: Wed, 12 Feb 2025 23:32:59 GMT  
		Size: 109.2 KB (109181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
