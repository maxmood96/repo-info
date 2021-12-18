## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:e5c802f5cac65c8e26000f4b971624b5d0acc12a2a55a2575591fd2e742bdf94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.405; amd64

```console
$ docker pull eclipse-temurin@sha256:3a23ad659519f7a3217bc7da776c65cba34a71b8a3ead7134999c47412c1058f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217571090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5e9feecd296a9da0800b7e97a232f26fe7b0e8fcd508348482012c46e764bf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 08 Dec 2021 01:24:33 GMT
RUN Apply image ltsc2022-amd64
# Sat, 18 Dec 2021 06:03:19 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 06:03:20 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Sat, 18 Dec 2021 06:03:20 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 18 Dec 2021 06:03:21 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 06:03:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 18 Dec 2021 06:03:36 GMT
USER ContainerUser
# Sat, 18 Dec 2021 06:03:47 GMT
COPY dir:7d20e7860b874019800a6393f3930849559cf997f64b86d2d0263d858293fa37 in C:\openjdk-8 
# Sat, 18 Dec 2021 06:04:01 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:11961e4f2e13a442b572d4bc37edfe94ad6d8c2ed378f0dcae8b880959c4b538`  
		Size: 117.2 MB (117225770 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:29e118c52df9d671b57a04fe35f79f686c3a7038ccd41c5bf5ccfac737426ab6`  
		Last Modified: Sat, 18 Dec 2021 06:41:30 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5b7a5eecd506c47a57cc6739d84cb5c60af0d1380a2d5f957caf673b1bbc77`  
		Last Modified: Sat, 18 Dec 2021 06:41:30 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6bcb7659e28871ad274e216b2bdcb65931330524d33dd748c004f29448c475`  
		Last Modified: Sat, 18 Dec 2021 06:41:30 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaae7decf72e8787f9547385a4d83910f4ce6a5082571946b9ceb524c792c181`  
		Last Modified: Sat, 18 Dec 2021 06:41:28 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb638b1165f6be88df12dba00424796a95a755cb648664a1f955668b299b27f`  
		Last Modified: Sat, 18 Dec 2021 06:41:28 GMT  
		Size: 87.7 KB (87709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5c0ec7254dbde449fa61bb0d02360f1eb3022551679da0f71fe1dd1decf410`  
		Last Modified: Sat, 18 Dec 2021 06:41:28 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae35fdac781e82ee82a059718dc8dbb1fbc3e5e52e950e0ce68301f15203a48`  
		Last Modified: Sat, 18 Dec 2021 06:43:17 GMT  
		Size: 100.2 MB (100190916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e68f0562a07681d687ff5a5d70b53305bded9500dbe1cd1ffd3379be6259a9`  
		Last Modified: Sat, 18 Dec 2021 06:41:28 GMT  
		Size: 60.9 KB (60882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.2366; amd64

```console
$ docker pull eclipse-temurin@sha256:d54e3be8e0953c00b5e4311a1fb22ad628c42e4b5aee771e340db4c8e470ab1f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203217797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838a921e8d0f8926de13aaf7d3e734a9a0943b1bacdb282609e30904056a1fe8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 05:18:44 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 05:18:45 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Sat, 18 Dec 2021 05:18:46 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 18 Dec 2021 05:18:47 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 05:19:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 18 Dec 2021 05:19:01 GMT
USER ContainerUser
# Sat, 18 Dec 2021 05:19:12 GMT
COPY dir:7d20e7860b874019800a6393f3930849559cf997f64b86d2d0263d858293fa37 in C:\openjdk-8 
# Sat, 18 Dec 2021 05:19:26 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4c557aac927613dd487d7c04b01a8eeb8ad174693f61b14c8f4285f1db6afdd2`  
		Last Modified: Sat, 18 Dec 2021 06:13:05 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6973854d52525a234a54d48939788fd0608bbfff1bbe6e466cc3d6059de3cf60`  
		Last Modified: Sat, 18 Dec 2021 06:13:05 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c369e58be1eac69cb5dcc0132f097abea84d2e8c69808085152940217a65c3`  
		Last Modified: Sat, 18 Dec 2021 06:13:05 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5d88585a1300485fe0cbd72e5c55f6e15245440aad16d70428ce08b23ab59f`  
		Last Modified: Sat, 18 Dec 2021 06:13:02 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524e248128bc58e6b08210a484684b98fca3d898dd34e4e346510ff3152e6e18`  
		Last Modified: Sat, 18 Dec 2021 06:13:02 GMT  
		Size: 74.5 KB (74538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bdecfa1b5609eca619389760d29e1491fab5f65b6992f484eec18b6f0cd610`  
		Last Modified: Sat, 18 Dec 2021 06:13:03 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826f8ef6f1d64157c3392cdf12f98a1472ed18231028a3d34164a6678f7915e0`  
		Last Modified: Sat, 18 Dec 2021 06:13:15 GMT  
		Size: 100.2 MB (100184358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f90140d1bdbb58e10160122a16fd34b83681b6aaa823ad4c1c46911282ebae`  
		Last Modified: Sat, 18 Dec 2021 06:13:02 GMT  
		Size: 49.2 KB (49179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
