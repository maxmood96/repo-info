## `eclipse-temurin:16-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:73a3d187a3e8ee0753820b4345c23b880f1b874ee627c5d90b6e81535afa0471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `eclipse-temurin:16-jdk-nanoserver-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull eclipse-temurin@sha256:911eb6d96ba40b13b667b08afb5550887d510bf515bebe06771dad5c5eb55acc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305542323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9844ac9fc5e5832679d5b4ca3dc7047785b5b91b37622cb16fa43872ff21a445`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:33:30 GMT
SHELL [cmd /s /c]
# Tue, 11 Jan 2022 22:05:16 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Tue, 11 Jan 2022 22:05:17 GMT
ENV JAVA_HOME=C:\openjdk-16
# Tue, 11 Jan 2022 22:05:17 GMT
USER ContainerAdministrator
# Tue, 11 Jan 2022 22:05:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Jan 2022 22:05:28 GMT
USER ContainerUser
# Tue, 11 Jan 2022 22:06:03 GMT
COPY dir:9a7ef5975d9ba9576c4744dc049616bbcb218f14c3c0bd967851cd46479d6134 in C:\openjdk-16 
# Tue, 11 Jan 2022 22:06:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Jan 2022 22:06:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6cc5785ab09c66739c3205c3a26410f1cf4bf85c377fa81b240e754cf0659c58`  
		Last Modified: Tue, 11 Jan 2022 22:44:40 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c2b42a2fc00f3ff7bee2e4d8d3c24a66f88055a3ee6d7c2f610d3cd8364ee9`  
		Last Modified: Tue, 11 Jan 2022 23:02:37 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e084d677b3d9d6e853c966e90a3e3e24aa547c35c9f36d035eb20dcb6cd0e63`  
		Last Modified: Tue, 11 Jan 2022 23:02:37 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c6aa86294060e9fcb7024109233078bc859132654a6579e36c9b19a3201d4b`  
		Last Modified: Tue, 11 Jan 2022 23:02:36 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d56ffc1947fc79dbe7d8cb64fee41f8a8d1e70c77488ff381059f65d3a589`  
		Last Modified: Tue, 11 Jan 2022 23:02:34 GMT  
		Size: 69.1 KB (69107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3ff926b6b1d46a7465a816e6859968a8a1836639c72533446916102b26c7f1`  
		Last Modified: Tue, 11 Jan 2022 23:02:35 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de799b369ee0549d25ad049062cb9d09bed7fd2fb1bdd428da77508386703aeb`  
		Last Modified: Tue, 11 Jan 2022 23:02:55 GMT  
		Size: 198.8 MB (198761564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b017a416dab87764e08bc7cf4c294685c16d0edd99d12d378d7459307fc5f928`  
		Last Modified: Tue, 11 Jan 2022 23:02:38 GMT  
		Size: 3.7 MB (3690694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2906e217daf3cebc318bffdafe863ebdd5c5945f5616001018de6ee486d364`  
		Last Modified: Tue, 11 Jan 2022 23:02:34 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
