## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d17671a92c8f3878179c4c6d20940e62f59c8295b611224cdbdd283de5ee8e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.405; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.405; amd64

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
