## `eclipse-temurin:25-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:733a2a688d885c819d4a787cd01130845e2471ad38af1935a23e2561c701763b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:baeb9e46f37804fa1983a6c4098ae1f2185c562610d7392a30869d9be2d5cee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185830936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed3387000bdb798682390feacdf64850c904bd41ca7927875dbf00d101141c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:32 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:25:21 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Wed, 13 May 2026 00:25:21 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 13 May 2026 00:25:21 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:25:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:25:23 GMT
USER ContainerUser
# Wed, 13 May 2026 00:25:27 GMT
COPY dir:fd8baea77fa86bd13952f69621f69e815eb87406af0c0441c94fb1b8a78482df in C:\openjdk-25 
# Wed, 13 May 2026 00:25:30 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03cbcd303d3a3d248ab22d617e183ed76d01abedfee5c52cc9fb7f6a87170f0`  
		Last Modified: Wed, 13 May 2026 00:23:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fc7a4bf3c8b1485de645c672c29e0e5703d098066bf18b38babd40daf48080`  
		Last Modified: Wed, 13 May 2026 00:25:35 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee61350fc5b86830996a3f9ff2c983b43612c68a878e17bf061f450d1cb9ade`  
		Last Modified: Wed, 13 May 2026 00:25:35 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dd359fbc4018fe9f1e15e52fcd580f035dae1fbf37f00b7b9f86b21346bca5`  
		Last Modified: Wed, 13 May 2026 00:25:34 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4100cf6c11f041b268817e47d8c7c55375ee5ddcf54e3973146cd84eab780389`  
		Last Modified: Wed, 13 May 2026 00:25:34 GMT  
		Size: 76.9 KB (76852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4667a61cdbea8b001e371c3b299e356cca7ed608ed39eb980839c26b70a9da1b`  
		Last Modified: Wed, 13 May 2026 00:25:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0cb344faca117c473db6d9d83b5aceb192c95587d75484ae0507b1d41cad52`  
		Last Modified: Wed, 13 May 2026 00:25:42 GMT  
		Size: 58.6 MB (58619970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e22b084692b6fa57e2c1d4aa5a564de0227e93ef050735e828cd105d57b6a7`  
		Last Modified: Wed, 13 May 2026 00:25:34 GMT  
		Size: 90.1 KB (90065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
