## `eclipse-temurin:8-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0da9a201d56339b4a9e2d9db87f4cc38b8952ab47d58ade1b488b26dfc6c10fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:8-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:fde05a2bbd00773f7e1c9b9c4ece63eedd8dd1c21a6534115c9372cc0726a14f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301661988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33982bf4ca4780d5752d8bddc3ed7578b5a748043c5b03874a7ece68683039c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 03:15:56 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 03:15:56 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 03:15:57 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 31 Jan 2025 03:15:57 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 03:16:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 03:16:00 GMT
USER ContainerUser
# Fri, 31 Jan 2025 03:16:05 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Fri, 31 Jan 2025 03:16:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793e8ff39f5df87ba6515d6f31d5cf83a480b3848a5cd6f5df7d0ce000cd212c`  
		Last Modified: Fri, 31 Jan 2025 03:16:15 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e622a732f67fd919ffa3deab5a2305958815f9d47d9eab6931ad9e7f9c60467`  
		Last Modified: Fri, 31 Jan 2025 03:16:15 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c9b1ca0281d4382dba07d8f3557e7cc8ee3d23dbeae632e0d74ebba7d8267`  
		Last Modified: Fri, 31 Jan 2025 03:16:15 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be705282eba0d497833387feab5bfb71dc4b058723c04aeba0fc9b17d1220926`  
		Last Modified: Fri, 31 Jan 2025 03:16:13 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285184abab11ecb74325a3d3bae2f5f2e4c187e644a11c530067a355d390c5e3`  
		Last Modified: Fri, 31 Jan 2025 03:16:13 GMT  
		Size: 76.2 KB (76245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c5466f9e9f11a9c15e1fe7abe05624b539f7e43ff1aa56ae2e1260863d8db3`  
		Last Modified: Fri, 31 Jan 2025 03:16:13 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02932b11f18241479d4b69e520ff3e2475b72291a754d9083161edca1c288c6b`  
		Last Modified: Fri, 31 Jan 2025 03:16:20 GMT  
		Size: 102.4 MB (102433321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7932a4a5c73937f1abc6a554f6a3fbf6204c05d9ee026f3c9bb65283f67a115`  
		Last Modified: Fri, 31 Jan 2025 03:16:13 GMT  
		Size: 92.9 KB (92874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
