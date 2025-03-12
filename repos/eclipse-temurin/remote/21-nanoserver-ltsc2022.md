## `eclipse-temurin:21-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8cd0cefd904e309484750a905641054eaf604aca4c7cbac8b104b047f1deb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:21-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:c1cb12141daafbca65ed33d17d8528e90083b28d363232ae76079f4f3628b4a4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322361273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36aa88539e50413b5f50398d81cea6490c2eb6680cc2ff88d5c46dbd2133ae99`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:21:15 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:21:16 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 19:21:17 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 12 Mar 2025 19:21:18 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:21:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:21:21 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:21:29 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Wed, 12 Mar 2025 19:21:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:21:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8cfb411f0d924614195c4591d3fbd5748c8568f99c75da90b13cd30d50f912`  
		Last Modified: Wed, 12 Mar 2025 19:21:38 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3843ef4f4640ee229b83a9df130defb616770d9db95c21f18d0753fb9e36abd6`  
		Last Modified: Wed, 12 Mar 2025 19:21:38 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7482bfdfc51a0d083a0e2528aa419005e17c3157532a6daa8c945c9da2eff418`  
		Last Modified: Wed, 12 Mar 2025 19:21:37 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3d74c986f892c1a2bca8cf2bf7d6bba8874e0280a0a9022ac85784425191c6`  
		Last Modified: Wed, 12 Mar 2025 19:21:38 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af68a7d718c79b53e5857f28b22419a5b934331e8543f04bbdf697d7ba868b4`  
		Last Modified: Wed, 12 Mar 2025 19:21:37 GMT  
		Size: 76.6 KB (76635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d51f6b18bbb59aa6234630061fc587429740422a209741efe462069c6ac33e`  
		Last Modified: Wed, 12 Mar 2025 19:21:36 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27942e712f377ddbf70184d1180cd29cf7ad819df5c0871c9e80518f079a2f05`  
		Last Modified: Wed, 12 Mar 2025 19:21:48 GMT  
		Size: 201.5 MB (201475584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5ef297db8830846f2aed41cca0d2b0af2a10a32834aba6f835979234699f18`  
		Last Modified: Wed, 12 Mar 2025 19:21:37 GMT  
		Size: 107.3 KB (107294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbbc8bc8cc517b4c160529d580403b3fd75357e43047f60d8e25e26f97f8f88`  
		Last Modified: Wed, 12 Mar 2025 19:21:37 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
