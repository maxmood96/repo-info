## `eclipse-temurin:24-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c88e4d1a9418f71dbf61949de7a76ba84e283d82ea327592e0e62b1a45866112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:24-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:09979de35a04494382df3ef8c9e4e35dd7d98fe8d577fc089616f5ed21d7a142
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180521220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364b522cb6ce7760f7beb00f711a76d1b1df780a0bf201d1d1bb39c94955e1ca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:12:46 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:12:48 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 09 Jul 2025 19:12:49 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Jul 2025 19:12:50 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:12:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:12:55 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:13:00 GMT
COPY dir:ad5bc1bf6efc16ac6d52d57c1c7046f6f9b2ef9ef08387497ec457eb9554ce7d in C:\openjdk-24 
# Wed, 09 Jul 2025 19:13:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523495ebee5dcb9e008f7e89c0b0cce46a22c3c322dc6c17f2ad6e88805d38a`  
		Last Modified: Wed, 09 Jul 2025 19:13:27 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a03cb9b228f2b23a5bd153f44316485416ff3c49812439f47b54b67c01240d`  
		Last Modified: Wed, 09 Jul 2025 19:13:28 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7816e1cb3662c8c5561c0aaa7d2f147c54704222888b1c456cfc7ace5f3a1f7c`  
		Last Modified: Wed, 09 Jul 2025 19:13:27 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4141469d4b9e96554fb35b66b9b09bb76c03fe8916c480eb9f28c92801ca63f2`  
		Last Modified: Wed, 09 Jul 2025 19:13:27 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ecb0bbc5383c11d8bfaab299a450666881967af5e8ff1320b667eda9e30600`  
		Last Modified: Wed, 09 Jul 2025 19:13:27 GMT  
		Size: 78.4 KB (78376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bf5df8e030f52f8044406533321ea98f97dc73e67cf877f3c383adf7aea875`  
		Last Modified: Wed, 09 Jul 2025 19:13:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8bb4b156ede44f476d0a7a6237c10216a61b7c2f14ddf8bdc823c0d808a475`  
		Last Modified: Wed, 09 Jul 2025 19:13:34 GMT  
		Size: 57.7 MB (57709030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b624ae9b80fd79eb8772d7aacdc7fe514c36f6ec84a8fafb3bae26e570a7968`  
		Last Modified: Wed, 09 Jul 2025 19:13:28 GMT  
		Size: 97.7 KB (97732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
