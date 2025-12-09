## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6a448aa46a4bbfa8f57286e5e758742de4f5ba2b2e48c7b6ecbb4a090563caa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:06a4c439051ac9ba5b0c30c83f7a2d88fee38739f00d61787b10008221a286b3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301523617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1c4c27a8960e46c25d167c883a66efbc97c688a4329e8dc0b1fe100d4924cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 21:12:48 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:12:48 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 09 Dec 2025 21:12:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Dec 2025 21:12:49 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:12:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:12:53 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:13:08 GMT
COPY dir:2635c350952b93f594bde5c3dd80336e4c4ce35889642cd7d3de9ae358e6cda3 in C:\openjdk-8 
# Tue, 09 Dec 2025 21:13:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acfb819e594e1d08813b5a2124af39d689e54a1c03ce6e66c31fd39ac284a05`  
		Last Modified: Tue, 09 Dec 2025 21:13:34 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3511784487da0bbb30ad609af37eeb615d58de0ef24091695f13f0276ccbdebf`  
		Last Modified: Tue, 09 Dec 2025 21:13:34 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d235b9c0a5d33ce1aef1c87747368a12dd939ebafb77d37cafe19fed8e7ca2be`  
		Last Modified: Tue, 09 Dec 2025 21:13:35 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dd07ad9fa47cc27c2d4bf2e589123efeec3f42c5f59c39022bdd0981f2780d`  
		Last Modified: Tue, 09 Dec 2025 21:13:34 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921dddb5fc60b9e3ac5caa2cb593314ce01e7614b38e3af69fe532ec70f5c6d1`  
		Last Modified: Tue, 09 Dec 2025 21:13:34 GMT  
		Size: 71.9 KB (71893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c851fa3e16ea0eb2c120b7fb7ab106897cc5cd8a9082d35c11cbc77ec33ff4a`  
		Last Modified: Tue, 09 Dec 2025 21:13:34 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c050df746cba7db6f6dd1797d82134dc05a2c7c389d3b51b3a583659f2ce53e`  
		Last Modified: Tue, 09 Dec 2025 21:13:42 GMT  
		Size: 102.4 MB (102438094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd4f22ce9925c54fa50010822653d8de62a321e602e1a290cf296e972c42b57`  
		Last Modified: Tue, 09 Dec 2025 21:13:34 GMT  
		Size: 134.4 KB (134368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.4529; amd64

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
