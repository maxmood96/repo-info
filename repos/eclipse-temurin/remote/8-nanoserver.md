## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b44f64a728d41fdd36dd7fb09ac3bd3ca5baee39d5985debdded1a5dee444d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:fdc76d68a4ade31b1458e8bd7dd7f394bb12be6960d4323f7f8153172c8a4061
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222746263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b73261c27535851115584aea38d9ffb6549611165b2f2436887bc497222a0d0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 07:21:30 GMT
RUN Apply image 10.0.20348.1249
# Tue, 08 Nov 2022 19:27:23 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 19:27:24 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 08 Nov 2022 19:27:25 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 08 Nov 2022 19:27:25 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 19:27:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 19:27:43 GMT
USER ContainerUser
# Tue, 08 Nov 2022 19:27:54 GMT
COPY dir:3f9950b949d84f617218d6370bf5d9344385a96fee23c5d0245f1523c4ce092b in C:\openjdk-8 
# Tue, 08 Nov 2022 19:28:42 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:72e5d750fe8c1a32d4a26ef3b4a4e1f6124ac079b142f12724af2abfcba1c8b3`  
		Last Modified: Tue, 08 Nov 2022 19:57:58 GMT  
		Size: 122.1 MB (122092167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd83067a7e6c6d9dab3ac0265a21919de95a0bf4e737e647fbf3e43c9874b0`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220e123f23808745fc630305de0ce242cb9a6c565cf4f700e22655ecf005687`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c25f1362ec097d0956355257914a48a3b53f55e8671e01cef2b0e3c09c2da4`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3937de06541d6c6a90657c15b73a603495a8d9f762eef4c868205c91c8dbb15c`  
		Last Modified: Tue, 08 Nov 2022 19:57:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d7087dd3a321a3aacf542b973f32ba8201f01dbb83c2cb89d350df169b7628`  
		Last Modified: Tue, 08 Nov 2022 19:57:25 GMT  
		Size: 79.6 KB (79630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375446a6e44c1ad04d6728e1b203b940f5a24bcbc2be35a789b03c1d5dabfabd`  
		Last Modified: Tue, 08 Nov 2022 19:57:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34772dce1f6b3f9671e813b130936e7c79e286e66ce2cfdc4159942e3bc840ec`  
		Last Modified: Tue, 08 Nov 2022 19:57:42 GMT  
		Size: 100.5 MB (100490566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790437c0068600c1ee6d15d7c04f6a474bfa6393faf17efe6dc51a455cfec718`  
		Last Modified: Tue, 08 Nov 2022 19:57:25 GMT  
		Size: 78.2 KB (78190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.3650; amd64

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
