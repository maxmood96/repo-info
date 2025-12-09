## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:16eb19c50b1c3a66f9287c766f236f2a4a72bfd981aa0fe02e40fed22bead7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:af2e5eae809d6859125c2b1bd0e7f51f0d6a16adc4f8e8a0651281d28af0078c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228977816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e56d2afb9aadcd64e78ecef83eee96d2f0a18ad1ea5ff9e2ea0230c606bf1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:25 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:12:25 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 09 Dec 2025 21:12:26 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Dec 2025 21:12:26 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:12:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:12:28 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:12:34 GMT
COPY dir:2635c350952b93f594bde5c3dd80336e4c4ce35889642cd7d3de9ae358e6cda3 in C:\openjdk-8 
# Tue, 09 Dec 2025 21:12:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa663d3f16715c8a3f881b4893114a8cb6d72761f93c48732d706cfc04ebee61`  
		Last Modified: Tue, 09 Dec 2025 21:13:04 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1d00b7705abadf1b5e8e8a7e56b82b04aae818ff89f9c754fcec1873309598`  
		Last Modified: Tue, 09 Dec 2025 21:13:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de6fa366e75ed3a74e4f5ccf30e603a8284cf7ba137d26319114796864fffd5`  
		Last Modified: Tue, 09 Dec 2025 21:13:04 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6bc0a54c7896b35c80167705916231f9bba8d6f372f39e050defd7bdd7624fb`  
		Last Modified: Tue, 09 Dec 2025 21:13:04 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800ff43a2c53729037518796a32b5d5391a3b15c3bd3e076dded72a549a0e86a`  
		Last Modified: Tue, 09 Dec 2025 21:13:04 GMT  
		Size: 75.4 KB (75404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7949bc4e6d286ffd88b6d3710e1441bb7c4b8f148db6205cc2966d0d1b424dfc`  
		Last Modified: Tue, 09 Dec 2025 21:13:04 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3094812497b870920fb48c4cfa0d900bee86e8bec21065e6810bc780a864b46f`  
		Last Modified: Tue, 09 Dec 2025 21:13:30 GMT  
		Size: 102.4 MB (102438046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25bc114b72067afa194e78efb563709571ace81c12ca7d1e4d6d9b1dfa1c2ab`  
		Last Modified: Tue, 09 Dec 2025 21:13:04 GMT  
		Size: 100.8 KB (100774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
