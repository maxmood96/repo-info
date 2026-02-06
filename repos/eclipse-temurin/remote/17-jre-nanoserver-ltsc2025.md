## `eclipse-temurin:17-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:aa0f55718d3c157003765a6693ebf3aaf7b081d791834b4af3fe7a56dd034fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:abd7c1bef9250799ffcb3318321fc5a836f1c8568872855c43ca948e0f6f4394
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243050882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de862f9c39a29e58a0d9973770ab13da1fa2166cca10bf8bec86e5fd310ea5d1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:39:41 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:42 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:39:42 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 05 Feb 2026 22:39:43 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:39:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:39:48 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:39:57 GMT
COPY dir:064fca0b30194d02fe341355ba6a62fc1748c82418561395eb5bec357779f4c8 in C:\openjdk-17 
# Thu, 05 Feb 2026 22:40:01 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b874dbe1b67df38e02528be3360c32428c65a1a9090bdab407a40bfb45c79c`  
		Last Modified: Thu, 05 Feb 2026 22:40:07 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25c267f1005db831474b51874742e0d80f836192da5c1c2f4030e25226e1de9`  
		Last Modified: Thu, 05 Feb 2026 22:40:07 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ae57978e9686da2c10e4f68a4671f779319dfbd90a0b8ab12271a3b3a17b37`  
		Last Modified: Thu, 05 Feb 2026 22:40:07 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ea36d16c805f171860be6f66d7033ba03e548b7e677252b43db86725e5ea3`  
		Last Modified: Thu, 05 Feb 2026 22:40:05 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025e05bbe80c402ff07158adec32cc1f32919520fbd3ff81336d569ab108cc45`  
		Last Modified: Thu, 05 Feb 2026 22:40:05 GMT  
		Size: 71.1 KB (71088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c77b8556dcdf9c618a902921edcba5f49a3a197abe6dfef721e5c76064c47c6`  
		Last Modified: Thu, 05 Feb 2026 22:40:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60eb44f5eede82caeee5eec822ca05be0b21021a82669d81782b9ec98c02799`  
		Last Modified: Thu, 05 Feb 2026 22:40:11 GMT  
		Size: 43.8 MB (43794924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ad984b96e4ffd71db72c15e66abcf783c7679ce3f9a1faf224fcdd4849069c`  
		Last Modified: Thu, 05 Feb 2026 22:40:05 GMT  
		Size: 103.0 KB (103016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
