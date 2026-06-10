## `eclipse-temurin:25-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:008a29d43b80d9859497e971cd1f2291fbc8d0593acaad4348cd4fdc82e96cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `eclipse-temurin:25-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:3690274f2789e24aa98bc0f5b89a4e4293fd2509745402cfe1f927a95cc4f3e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 MB (334883161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bc1a2ea86d026655e866d6d8ed15e9bbade15119855dc8b0c9dc676c12eb05`
-	Default Command: `["jshell"]`
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
# Tue, 09 Jun 2026 23:19:30 GMT
COPY dir:93c9a33f6e3b7bf9a4cc6584352427179a8f4d1e9396155b43179dd1c4270396 in C:\openjdk-25 
# Tue, 09 Jun 2026 23:19:35 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Jun 2026 23:19:35 GMT
CMD ["jshell"]
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
	-	`sha256:2a31501229c4d2a9f99a7a33cc8ff9fa8ae2d953db8a59c9230008b0894a72a0`  
		Last Modified: Tue, 09 Jun 2026 23:19:52 GMT  
		Size: 138.0 MB (138009066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f8605f83de41081a328c42a61bc907b5cee993d5a9f9159bfe5a69baf77f85`  
		Last Modified: Tue, 09 Jun 2026 23:19:39 GMT  
		Size: 127.6 KB (127609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a841212ad4e62f992b47a399051250566cfd0e9e95711012afc03d4c8eb6b7`  
		Last Modified: Tue, 09 Jun 2026 23:19:39 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
