## `eclipse-temurin:8-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:c81c43178bb397ce90c37b05fb15df5ca6763eb4ca4c3730e27cd8b7d939bf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `eclipse-temurin:8-nanoserver-1809` - windows version 10.0.17763.2366; amd64

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
