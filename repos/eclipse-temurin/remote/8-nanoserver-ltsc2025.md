## `eclipse-temurin:8-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:3ffdb83ecc3b7e51c358472d544bdca799f986b90f311823f57a19871a538b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `eclipse-temurin:8-nanoserver-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull eclipse-temurin@sha256:1fde0c0c91c2d1d3f56fda73a8eee65d37401a363904bb4f015e3842b6702b2f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300566854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cacdcd7f6a5f4fd76acbd2006f0f2c85b63d89f7df6b9cca44e8b5f69cf6860`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 11 Nov 2025 20:10:57 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:10:58 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 11 Nov 2025 20:10:58 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 11 Nov 2025 20:10:59 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:11:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:11:07 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:11:18 GMT
COPY dir:2635c350952b93f594bde5c3dd80336e4c4ce35889642cd7d3de9ae358e6cda3 in C:\openjdk-8 
# Tue, 11 Nov 2025 20:11:23 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3719b064c723247381b30c79062f31cb652086c11ba8db976957ea55feb01df4`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e152bb5a47b72f5eb63867dc5531e98f5f99128e638467303d4524d91ab001`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a632a180fc75c8a20c0f059f18f179383c5228e4fda0babfe681c785faeacb`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385fc7ff0792f6b05dc6f4414779e6eb10027d5bd991f06fbcdf249b15f0b33a`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd17e42dba0eabaa2036b7cdad05a4907865bf2858aa5d6eddcd216f751042b`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 77.7 KB (77701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875d7b76e1ded141116d27f5ee83f559a7da665cf916063f1de85c6238f595e3`  
		Last Modified: Tue, 11 Nov 2025 20:12:16 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873c781d1969ec2132ed5eaf17f66f66b94207a6f2dba5102de9b818996176c6`  
		Last Modified: Tue, 11 Nov 2025 20:12:27 GMT  
		Size: 102.4 MB (102438305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7024a5f8f467f1844f21ed6e82dc497b580578ff4808f27f54335561a9f7be8`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 109.1 KB (109078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
