## `eclipse-temurin:8u492-b09-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:257d00c2611733e9f5bb2edb7621f6aaaafbc625988cc176239e2a83d5ae5d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `eclipse-temurin:8u492-b09-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:896dc212443cd624d88d3f2f28c8e7bee9454617b050cf3bcf50945790c7c06d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236861541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77477a67c27a160445c7e7849bfd00ff1e13e722bc29dbb1a33cf1d47418c550`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:20:15 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:20:15 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 09 Jun 2026 23:20:16 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Jun 2026 23:20:16 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:20:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:20:23 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:20:32 GMT
COPY dir:deea9cd49fa78c2b910137007aed467626dd46389507789da1635093de3df40f in C:\openjdk-8 
# Tue, 09 Jun 2026 23:20:37 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5bca1b431c3da1091eecc072ca1cdbeb98a20d58d24be4efc21735120a4e86`  
		Last Modified: Tue, 09 Jun 2026 23:20:43 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf901e8ea05d2a29c9c393cbdc2b4b2275002d8a8be1ca8be622cda21784332`  
		Last Modified: Tue, 09 Jun 2026 23:20:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09fbd845b83808e409f3b53765ee3f1986e47b4612048108cf02c6d3391e41a`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5eadea197797ffd3392da8c19927ed07e7789d1519d4e112f26417773a7c044`  
		Last Modified: Tue, 09 Jun 2026 23:20:41 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec904b8ed95a3e1546a9fb90d653e4b6e3015b5baba9a12b96412429d4fd570`  
		Last Modified: Tue, 09 Jun 2026 23:20:41 GMT  
		Size: 90.5 KB (90527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc0b111e19dbb66f59d1d6c64af4b5fd197fde0df199d2294529380e9137bb7`  
		Last Modified: Tue, 09 Jun 2026 23:20:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02650b75e99022f0862c9d8df68b8bc037a2aea9f570cf3656e3970de9924cc7`  
		Last Modified: Tue, 09 Jun 2026 23:20:45 GMT  
		Size: 40.0 MB (39988062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e0576ec497e60a8d81997ffc97d6a4e4e9c6392986794afac4ebe00d794aa5`  
		Last Modified: Tue, 09 Jun 2026 23:20:41 GMT  
		Size: 109.7 KB (109659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
