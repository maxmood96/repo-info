## `eclipse-temurin:24-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:544f8ff0c8496128d94a30b36112509c1eb6ab9184f4f44480868d43c7960da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:24-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:ecc380437119a1e4be75e1e6d30d9dd8f048a4d061ecb099f23bd2cd0b19bb8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180475938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ed0e0c1d01fa040b8f4ddcad6e12e5d4ee179dbcf8afdca6466049322125be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:18:16 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:18:16 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 14 May 2025 21:18:17 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 14 May 2025 21:18:18 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:18:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:18:21 GMT
USER ContainerUser
# Wed, 14 May 2025 21:18:25 GMT
COPY dir:ad5bc1bf6efc16ac6d52d57c1c7046f6f9b2ef9ef08387497ec457eb9554ce7d in C:\openjdk-24 
# Wed, 14 May 2025 21:18:34 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46ba21e7da548b9f9fc6989767bd1c0d452c4d90a72f1719c0a2d4c7197584c`  
		Last Modified: Wed, 14 May 2025 21:18:37 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341fa217f1891ff396ac83b7d82e3a6ef2671c9c2e49f1d568d10ac0d916d8fe`  
		Last Modified: Wed, 14 May 2025 21:18:37 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd11cce2f4722ad8e4725fb4cc238b0aba5ccfe1eb6e8d0f80611882bdeaf0a`  
		Last Modified: Wed, 14 May 2025 21:18:37 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fdf900aec46ca25025fd7ca4e0fbb428caee8a1bc5ca76aa6f52fc1b523fd8`  
		Last Modified: Wed, 14 May 2025 21:18:36 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9525eaffb6102ab9c31d7ce0eec5925496a8b58607a0c6217433d868894ad2e`  
		Last Modified: Wed, 14 May 2025 21:18:36 GMT  
		Size: 75.9 KB (75852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd6a9b2a1e43b549d0e8687594462da11793de375c7981fef0a26a4f7054381`  
		Last Modified: Wed, 14 May 2025 21:18:36 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e438a53b686c51cf8d2a0dd430f234e6613d98a1a88845899b0ccc8a89b8cd`  
		Last Modified: Wed, 14 May 2025 21:18:43 GMT  
		Size: 57.7 MB (57709309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6649873c0a6ba2ce2727710b21d27238ead19d2608775ee972fa598d7b6bbc0d`  
		Last Modified: Wed, 14 May 2025 21:18:36 GMT  
		Size: 109.0 KB (109013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
