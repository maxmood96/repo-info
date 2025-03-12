## `eclipse-temurin:23-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:02643800f1e2ee1d22ab28824d7ecee62251317f3c9fe0b2c0fe046338df731c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:23-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:76a871a4bad0270c8adf29c6d31cf7e5ba5d6607ff8774930bb13aca15a281db
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415542330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c41e31affc04a1a079c5483c066e826952382c2027ae9ea9660ecd2137c3a05`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:17:10 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:17:11 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 12 Mar 2025 19:17:13 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 12 Mar 2025 19:17:15 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:17:22 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:30 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Wed, 12 Mar 2025 19:17:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:17:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bf3c3542309e7f1d5728352eb25c5544785e5ee6e9ee048fe6358f67df791e`  
		Last Modified: Wed, 12 Mar 2025 19:17:43 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d3622ca71fda8d23fee1e0871fcba44ebdd584716dda853fdc67b2a58c4e2`  
		Last Modified: Wed, 12 Mar 2025 19:17:43 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8913103197db4778e1a9567b916c6fd74c0df05527a4f3cc4e964149ef739641`  
		Last Modified: Wed, 12 Mar 2025 19:17:43 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48356f74a40d035851128ab860c4bd353c3002d7a008a3274e29bb0e91298c3e`  
		Last Modified: Wed, 12 Mar 2025 19:17:43 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17f88f196234a4db067428f8767ae60f76c85ff1d26a4d8dfa86379a61b58fa`  
		Last Modified: Wed, 12 Mar 2025 19:17:42 GMT  
		Size: 78.0 KB (78004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af6aa9621f82fecc4747ac5fe607cf8ddb161df5506530a65ef54eb10f7bf6`  
		Last Modified: Wed, 12 Mar 2025 19:17:42 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58266192d4250a20831c50ad8163d749b7d8ccd15c7ab702878480ef3469ecdd`  
		Last Modified: Wed, 12 Mar 2025 19:17:54 GMT  
		Size: 209.0 MB (209029484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bfe8685f0408c6b9049e7a4918318ba4b15449a010e60169dded314b14cfd`  
		Last Modified: Wed, 12 Mar 2025 19:17:42 GMT  
		Size: 126.3 KB (126297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecba42d76a865f68b0c26f87b05075833047c1538e4c6d64fda40c7fda76ebd`  
		Last Modified: Wed, 12 Mar 2025 19:17:42 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
