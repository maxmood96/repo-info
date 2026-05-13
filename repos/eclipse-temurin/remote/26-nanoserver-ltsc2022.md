## `eclipse-temurin:26-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c056dd99f02ec80f47ed2d5b84a9fd360e80415f5f12937b11d4b98bbb1d4e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:26-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:fe991dee779aa26edb7abd03c55318ca6f50fad0ccd7807639eaf2de8fe2fcff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268549276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9336d5d6417d8f87d2d7845816528fa31e74df2f8b28826663f7fd68060d2a7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:53 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:25:44 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 13 May 2026 00:25:45 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 13 May 2026 00:25:45 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:25:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:25:47 GMT
USER ContainerUser
# Wed, 13 May 2026 00:25:54 GMT
COPY dir:8f93d89558d485d03b81034182d43f2557754598b0731c760b32ca0af365b3c1 in C:\openjdk-26 
# Wed, 13 May 2026 00:25:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 May 2026 00:26:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268beb93bae0a3fcb4f27b79193145978fd732af03aac83a53212232ff073dca`  
		Last Modified: Wed, 13 May 2026 00:24:15 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4acebb6f42e7f6ef398f5a76db76007206a9287a466ee6ab171c08b4695a05`  
		Last Modified: Wed, 13 May 2026 00:26:05 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a432d57cd7e5da2cf6b2eeb547993841675a45b2a32014d478f6f3cb3bea4bfb`  
		Last Modified: Wed, 13 May 2026 00:26:05 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a093488e817def8a04d4164d686b4e580b2d8d5652b21de4ca1d976a023ece76`  
		Last Modified: Wed, 13 May 2026 00:26:05 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515e76fa2b446d0e9fa327c93e48a87deb2b22eaa57b6908ca8c8ab6a63e6890`  
		Last Modified: Wed, 13 May 2026 00:26:04 GMT  
		Size: 77.5 KB (77484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e63e0b9130231609355b278250383747a6447fbe156185a31e092aa863475b`  
		Last Modified: Wed, 13 May 2026 00:26:03 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f89218b2bd164348369ab132d0182aeb608956ca9f10cff2fe729fa5542de9`  
		Last Modified: Wed, 13 May 2026 00:26:17 GMT  
		Size: 141.3 MB (141306985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4878d75dcbeba0f2ef993e14edd54a40d2a03bfb43328b22fb8933d40763382`  
		Last Modified: Wed, 13 May 2026 00:26:03 GMT  
		Size: 119.6 KB (119649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1893e8aa73d0d00e9abdc30ba97accfbd55df70916c05b26fe65a106643fa070`  
		Last Modified: Wed, 13 May 2026 00:26:03 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
