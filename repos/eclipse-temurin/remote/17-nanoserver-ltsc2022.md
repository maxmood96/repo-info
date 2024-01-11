## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:53e440a657de59eebd9d1e5011710ae800ee8cfe99c63dbf33d4f8f88111a676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:d00c0e545297d7c1f005ce2e3de8b5be828d35e060b97a7bb30fb727b6288a11
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307588944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d77e9d11723918a4cc7306bd0d5f23036e7404cd65af780f0473eff0603afd0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 23:19:42 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Wed, 10 Jan 2024 23:19:43 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Jan 2024 23:19:43 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:19:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 23:19:54 GMT
USER ContainerUser
# Wed, 10 Jan 2024 23:20:09 GMT
COPY dir:abd8f71dbffdebb78ff7b01992fc9930e8aa0c6f2b1d8e6ad05b2a0c8da5ed1e in C:\openjdk-17 
# Wed, 10 Jan 2024 23:20:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Jan 2024 23:20:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5f2601f3a3b05b34c1f8683e3c9ea81ea63dbe1b04c37b85d09170f020fc0`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c0b41288d7a6dced95afaf6fe69fa8a0000dcbaff56e7f1d3e657e9cbd1f86`  
		Last Modified: Thu, 11 Jan 2024 04:20:26 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19ed1b114465c6285c07cee424dc0d2055f2f9ed3913a91e2fe3d894c95f2b7`  
		Last Modified: Thu, 11 Jan 2024 04:20:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1c7551f930b96326abc7cf55564fe9b20ec482df7c62f1c0bc253821fa5743`  
		Last Modified: Thu, 11 Jan 2024 04:20:25 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7608281d9daf7abcac939cb214476ed7b9bd942966d5f628325d372897231377`  
		Last Modified: Thu, 11 Jan 2024 04:20:24 GMT  
		Size: 78.9 KB (78947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee63e6da855b22ed10f2c0442e956225dfa84e60b8fe618ef5e840169cf85551`  
		Last Modified: Thu, 11 Jan 2024 04:20:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971784f12f7e29866d8ae07235719525613a8293b2a1e11346eee3a68e48c122`  
		Last Modified: Thu, 11 Jan 2024 04:20:43 GMT  
		Size: 186.7 MB (186658951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e84ce3bd7f3d51fefedd453f4d785759831bbed7afb4972858e1b5da81fe18`  
		Last Modified: Thu, 11 Jan 2024 04:20:23 GMT  
		Size: 74.9 KB (74853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045fd89ed631c3f6648ae01333fb397e59c156772b8f91237fbd59781f1833e2`  
		Last Modified: Thu, 11 Jan 2024 04:20:23 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
