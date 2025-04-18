## `eclipse-temurin:24_36-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0f9f2643ce00a4a1c6eafa0bfe393d115fba0534cfad53864b1a5b78d4c2f905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:24_36-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:3523229d86fbba79fb8660ac0d861f91bf6183ea471793cdb0e39d141ef9fdea
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260084739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0243202d486fd302bd69686d41bd3881e8278f3b549db8128920da54baf4b114`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:18:22 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:18:23 GMT
ENV JAVA_VERSION=jdk-24+36
# Fri, 18 Apr 2025 04:18:24 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 18 Apr 2025 04:18:25 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:18:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:18:28 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:18:34 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Fri, 18 Apr 2025 04:18:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:18:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7042c2e4442fc6e6b29d5c1cd91e3c0c2b415e76ac3de3430a75fbc20c42a3`  
		Last Modified: Fri, 18 Apr 2025 04:18:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a4db1978185809159ecf4eeb6510d679d6d362df6f190d4a9f5cda96d8f317`  
		Last Modified: Fri, 18 Apr 2025 04:18:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc4cd9445867348020310707d919c65754d4cbf4f01c64ecb20e138ff82d3d0`  
		Last Modified: Fri, 18 Apr 2025 04:18:44 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d79de9c9e8dfda389edfe81c84a25648e1139adb3acd154430915852adb86b`  
		Last Modified: Fri, 18 Apr 2025 04:18:44 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dacb06b332fdfa955837a963f1204b25922e8392334c834f7c81b1b47009a4`  
		Last Modified: Fri, 18 Apr 2025 04:18:43 GMT  
		Size: 77.0 KB (77022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60671a14b65fe221c93a418e3f485aa2d838de719ff1a0b0c1e47d045ffb06e5`  
		Last Modified: Fri, 18 Apr 2025 04:18:43 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23e0bfcc428513c565d86a0962b1663f29b4c68c911091abe5aa69d15a4a959`  
		Last Modified: Fri, 18 Apr 2025 04:18:53 GMT  
		Size: 137.4 MB (137355442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590ded974672f778e8ca546a5b6e682734bff3a240e71c53e0635538ade89829`  
		Last Modified: Fri, 18 Apr 2025 04:18:43 GMT  
		Size: 107.0 KB (107001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3723415a88bbee57fbbc0a52a96b6b8890db7578c6cac6a4b7744ef81f7673`  
		Last Modified: Fri, 18 Apr 2025 04:18:43 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
