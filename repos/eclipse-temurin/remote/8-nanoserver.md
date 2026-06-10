## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:025db2efa6703eefeae3e67d35bc88cd0f234c5666e32b15e09bb060a2b28816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.26100.32995; amd64

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

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:30af1c4b31fae957c656411b5f9621184534a9e08c04d91d06ac1699c9892579
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226131762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6ad350b52cfd9c7248c07277ad99fb83bd28abb37148bd3a29872ef5d7bc37`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:28 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:20:29 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 09 Jun 2026 23:20:30 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Jun 2026 23:20:31 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:20:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:20:39 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:21:04 GMT
COPY dir:25077d8770e7edce418eff57fe3a0561246eac55d5c42b7efa90e67ec851bbed in C:\openjdk-8 
# Tue, 09 Jun 2026 23:21:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c10a1597ccfac50e0bee5f1f86b66638570a85b10d64ac0590eb5ce44dac1bf`  
		Last Modified: Tue, 09 Jun 2026 23:21:15 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae61e10b5840701ec46695c0e37c0d49cd3f0f36522947b74af79912b254f6af`  
		Last Modified: Tue, 09 Jun 2026 23:21:15 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d277589199457d6ec8f85dc6440fb7cd80f352fd5bc0d5dda5db7d619ef2da31`  
		Last Modified: Tue, 09 Jun 2026 23:21:15 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634d1cb9dae1f95e0914e993998b21df550bb615affbd20e1ec01f507a447455`  
		Last Modified: Tue, 09 Jun 2026 23:21:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43285234d9aec68a3a8729c9db4779075b8ab6aea3fd8842060ca34daf7e508a`  
		Last Modified: Tue, 09 Jun 2026 23:21:14 GMT  
		Size: 85.5 KB (85486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cea5f8be39432fa6a930bba7583e46d5c6271939c0d89ca9a8ed68218c9e7ca`  
		Last Modified: Tue, 09 Jun 2026 23:21:14 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54f3476ceb9fd020eec55a5ee642d8bfd3791ced31b9243fdf8761deeab56d1`  
		Last Modified: Tue, 09 Jun 2026 23:21:21 GMT  
		Size: 101.9 MB (101915854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d3b339abdb76e8cb1abb4dff8488ac0a211106cfd1e359a6a263aaa42a6a7`  
		Last Modified: Tue, 09 Jun 2026 23:21:13 GMT  
		Size: 127.6 KB (127593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
