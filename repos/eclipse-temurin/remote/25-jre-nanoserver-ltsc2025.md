## `eclipse-temurin:25-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:01f5e53647fb139d16beee6484328e90e6783e51191a2c3eaf9f3282031e36f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:a5fc03d72668dad3242e699b928a00064c6d0e0664ccacf84cc4f0051ad4f595
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255470334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cf113898edb9a4d641b20059be69072041f588c8755fcec3f459ea2d3e1d08`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:18:08 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:19:09 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 09 Jun 2026 23:19:10 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 09 Jun 2026 23:19:10 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:19:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:19:12 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:20:26 GMT
COPY dir:fd8baea77fa86bd13952f69621f69e815eb87406af0c0441c94fb1b8a78482df in C:\openjdk-25 
# Tue, 09 Jun 2026 23:20:29 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee5a15e6c0ae33d8458f16b5e982a3e6eb3be95d54d8918eb8862671f3dd652`  
		Last Modified: Tue, 09 Jun 2026 23:18:35 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d434ce39a94cb42837489ac5f874e842e95c28229676a028d0657e3ddc3d013`  
		Last Modified: Tue, 09 Jun 2026 23:19:41 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1464cd31e07129fb4c5043089b75fe7aa75ede3af2d22f3f457c5c3b4f0ecd4d`  
		Last Modified: Tue, 09 Jun 2026 23:19:41 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864e1450bf94e58601592313310a4e3629bfde4f1201241a37247e2be054168f`  
		Last Modified: Tue, 09 Jun 2026 23:19:41 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa44cbfb3f8bad29f9e0693678d2233155c291af9be0c4d889bb258191e6557`  
		Last Modified: Tue, 09 Jun 2026 23:19:40 GMT  
		Size: 72.1 KB (72143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4074c51f5bb1638e60bae7da2d292dcba51153746120d25d4ba4d89c8cd3bc`  
		Last Modified: Tue, 09 Jun 2026 23:19:39 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0c8b9076860f258799fe381029ad2830d9edac336b1cd3102e80bcf8992830`  
		Last Modified: Tue, 09 Jun 2026 23:20:41 GMT  
		Size: 58.6 MB (58620328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9346b1f13af12bcaf732684338c0aa5d91937fd764109f79edf58c8bfcbe88ff`  
		Last Modified: Tue, 09 Jun 2026 23:20:33 GMT  
		Size: 104.6 KB (104556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
