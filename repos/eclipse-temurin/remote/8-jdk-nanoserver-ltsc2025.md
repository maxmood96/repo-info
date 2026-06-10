## `eclipse-temurin:8-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:af8cdb8b017c22e7a797c6ddf14c7b8d0b0268b04314f33b5b7ac1c7ddfd8c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:b0115f51d7b3ab3e91e77d6428584e9e77d8d6746c8a65b578111daa21d96284
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298762770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a1fde0423a3ef9f6cf820e4355c34f4fc98e26474efa84370a5822c37a1b68`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:20:14 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:20:15 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 09 Jun 2026 23:20:15 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Jun 2026 23:20:16 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:20:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:20:21 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:20:35 GMT
COPY dir:25077d8770e7edce418eff57fe3a0561246eac55d5c42b7efa90e67ec851bbed in C:\openjdk-8 
# Tue, 09 Jun 2026 23:20:41 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bad79892459f5dd7045f65a61fffc3ce3f1eb0f41d89a31326f6fb0fa55d14e`  
		Last Modified: Tue, 09 Jun 2026 23:20:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb45fb39326cddc3b80dbe1fddbf88ba94858f8d769595d4db14540a5ba5ab4c`  
		Last Modified: Tue, 09 Jun 2026 23:20:46 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72493f99f980363d3be9b8dfe70528d4a1704bfe65c7c8046a7c3d1ef4cc10f5`  
		Last Modified: Tue, 09 Jun 2026 23:20:46 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18be6e1ba6eb412931547ee53be82089f3ef73563f996debe1db4b208f8b8fe2`  
		Last Modified: Tue, 09 Jun 2026 23:20:45 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae8012057427b09d70fec65fc55f3b349c12b5e4440af08ea548db7035afcf3`  
		Last Modified: Tue, 09 Jun 2026 23:20:45 GMT  
		Size: 70.5 KB (70547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3d209388393c4046c84a4ac1beb13b24bb3d953aeb1fd98907a7bce1b5da69`  
		Last Modified: Tue, 09 Jun 2026 23:20:45 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6195b846fd1c2d5b00c3b2a659cc4cfd19c4afa8abad0f123825909e5ee8b4`  
		Last Modified: Tue, 09 Jun 2026 23:20:53 GMT  
		Size: 101.9 MB (101915878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce5b7b5ca0a1bf2232c8a6e1bb433966299877f723dea227873a269e64d0abb`  
		Last Modified: Tue, 09 Jun 2026 23:20:45 GMT  
		Size: 103.0 KB (103037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
