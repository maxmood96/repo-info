## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:3a8a00f2cbce29314c1c29756067c2bfcffc5ebf47eb6daf2db487a484d69426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull eclipse-temurin@sha256:f6ff5789e9f40973dba7328eb74db7b6b742c9618f2d2be07abe64ffc22ff0c7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207415734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcd236cc3c4049beb162a6a440c5343af66deec0a6589d5bb0c1c208187feda`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Tue, 08 Nov 2022 18:36:25 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 18:36:26 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 08 Nov 2022 18:36:26 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 08 Nov 2022 18:36:27 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 18:37:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 18:37:02 GMT
USER ContainerUser
# Tue, 08 Nov 2022 18:37:14 GMT
COPY dir:3f9950b949d84f617218d6370bf5d9344385a96fee23c5d0245f1523c4ce092b in C:\openjdk-8 
# Tue, 08 Nov 2022 18:37:40 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e8f4bb4b79b67857c1e4ac5c66026fd5ff5badbde5a8b59b11251b02699586`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c44dbc7f003b29fa4e1abb69635a1a6354a2c0cb49f6a9ff6dc4d1b639acc98`  
		Last Modified: Tue, 08 Nov 2022 19:44:53 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fb91c1a718c599d124b35a4ba105c41d65f391d68beed1eeb58e06660d8136`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b16510d59ce3bbef885f91367330f07ac32af4e3bbefee8ff015cd414d0646`  
		Last Modified: Tue, 08 Nov 2022 19:44:50 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63890e522e464b0c794c02a6277fb28ecc0bf6f1982be903f1f405e81d4c7490`  
		Last Modified: Tue, 08 Nov 2022 19:44:50 GMT  
		Size: 76.5 KB (76518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bffeb8602a05ed27d48cbfd978a4c71319ffe1209858cbbeda69470b489563`  
		Last Modified: Tue, 08 Nov 2022 19:44:50 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57de467861df2b42fb565bee1c29433f4b80b4e40312435844583ff2e821096f`  
		Last Modified: Tue, 08 Nov 2022 19:45:07 GMT  
		Size: 100.5 MB (100491002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a077ef424e90ffdd4100702b67b037860028a9ba6e7f7c0aa3c8b3a7e80edd`  
		Last Modified: Tue, 08 Nov 2022 19:44:50 GMT  
		Size: 119.5 KB (119465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
