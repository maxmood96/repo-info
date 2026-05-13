## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0691916885abbc26130d8d9b0f226bd93fe7397b9880b97179312c1ee1b45ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:22e20df57cec2c2c30bf84a7ac218b3c39a741b2645f120e06c2df4a2c57cc08
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322023212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3eeefc07f458d57e415188ee787eb91f34dad5b7fb6d39de25f95689367a34`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:53 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:23:54 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 13 May 2026 00:23:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 May 2026 00:23:55 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:23:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:23:57 GMT
USER ContainerUser
# Wed, 13 May 2026 00:24:04 GMT
COPY dir:508f69ae524938b28a83a19a9aeade10facf00325b620c7a836698644d966097 in C:\openjdk-11 
# Wed, 13 May 2026 00:24:09 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 May 2026 00:24:09 GMT
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
	-	`sha256:bf550725b6107dc6e48bc11fa422738baccab824cc9a9d10c4f9e31a6e2d03e3`  
		Last Modified: Wed, 13 May 2026 00:24:15 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bd1e3e74af70804518c5e1eb4739b56a2844b8f7809020f0d3d51131e78d34`  
		Last Modified: Wed, 13 May 2026 00:24:15 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290ccbff41a5373683686c8a520c1e7224cc6b265d90d8a6e1953fb02d161698`  
		Last Modified: Wed, 13 May 2026 00:24:15 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcfe9f830be9a7ebeddbd6595278839185772c20ed09db58e29fd3f2f119b2c`  
		Last Modified: Wed, 13 May 2026 00:24:14 GMT  
		Size: 88.4 KB (88434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996038cb0a0deff3cf0cbc3c29e9f19609d27cdfcd4491bd703a1addda0b9aba`  
		Last Modified: Wed, 13 May 2026 00:24:14 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca6916c4a08b95e3951b1abf5d4370d6a393f6d0272a6cd765efc162d0809fa`  
		Last Modified: Wed, 13 May 2026 00:24:27 GMT  
		Size: 194.8 MB (194785524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0123595c61b8d45eb3017b69e63108b8a04c465b88c0163a81cfb132ccb4e66b`  
		Last Modified: Wed, 13 May 2026 00:24:14 GMT  
		Size: 104.0 KB (103994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b17c49a178cdbdb4018237d00f58613bb7d9ead36a9bdfd68550ad43fc076eb`  
		Last Modified: Wed, 13 May 2026 00:24:13 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
