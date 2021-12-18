## `eclipse-temurin:8u312-b07-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:3587593408e6ad5384f70bd146581548d01cd469808c9caedb330dec3f5f1ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64

### `eclipse-temurin:8u312-b07-jre-nanoserver` - windows version 10.0.20348.405; amd64

```console
$ docker pull eclipse-temurin@sha256:0880bdf57e382be10e1d574c488b1b508a4d6f6d3d048c1133ac2fc2f928b54b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156471134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5f57b3e3f91636a63dff515ca5fedd31cd1004b17d6f0284925f3af90bf626`
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
# Sat, 18 Dec 2021 06:04:15 GMT
COPY dir:f43ebde5893522b38a147191e5e447aa435ef67c7d947aeb3e536f25bc61cdb3 in C:\openjdk-8 
# Sat, 18 Dec 2021 06:04:27 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:2d073cc08989f66620e38e92691279081d7e1f06ddca9e19779ec7371ae9c5d9`  
		Last Modified: Sat, 18 Dec 2021 06:44:11 GMT  
		Size: 39.1 MB (39090986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416018b4d7a945e7a3aa685645bfb8c1576c28faf48e92432cb6f2c065b7ec56`  
		Last Modified: Sat, 18 Dec 2021 06:43:29 GMT  
		Size: 60.9 KB (60856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u312-b07-jre-nanoserver` - windows version 10.0.17763.2366; amd64

```console
$ docker pull eclipse-temurin@sha256:bf2fde8d5b6d8f602f636f05ca8eb9aa6a6728c848f6c3582b1852b5054f3a6c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142123246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd440d28822121f0e3fc14a7b5818cd0a7e052240f9d3aeca9faed8abaed28bf`
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
# Sat, 18 Dec 2021 05:27:03 GMT
COPY dir:f43ebde5893522b38a147191e5e447aa435ef67c7d947aeb3e536f25bc61cdb3 in C:\openjdk-8 
# Sat, 18 Dec 2021 05:27:16 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:7b2c5235e005abf89e9569bb2aef7189f328e026f394f0301e088137183a247d`  
		Last Modified: Sat, 18 Dec 2021 06:14:38 GMT  
		Size: 39.1 MB (39090976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f47851105c507595cccaccf197fcae5085f32440e7d2399a31c83b002a94eb`  
		Last Modified: Sat, 18 Dec 2021 06:14:32 GMT  
		Size: 48.0 KB (48010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
