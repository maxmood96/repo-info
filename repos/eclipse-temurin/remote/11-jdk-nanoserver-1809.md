## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:fc88b1c0e5612eb21e7cebbdd4c22e37cd508b094d05e32e5cfcd61f67d27bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:3f3d8bea3103bbf28e55b447628f6a60ca22e4aa72552d754f4bf64f1dd1ad5a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301660202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8dd0107ce7727c7fdc08700c442573cb8d60126865e90ffc35277efb6165c7c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 02:21:07 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:21:09 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 09 Apr 2025 02:21:10 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Apr 2025 02:21:11 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:21:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 02:21:15 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:21:25 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Wed, 09 Apr 2025 02:21:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 02:21:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f009080a9c6c9d1c832e9e0ddc62d02797d24cd9458df88e4d868aa2d51500`  
		Last Modified: Wed, 09 Apr 2025 02:21:34 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0a3ccec1a2892c3c3ca164433689955a4aa993baf136a3a739ea0e9d9bcd5c`  
		Last Modified: Wed, 09 Apr 2025 02:21:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553efc26c3aed35afc60f221042d255f955e901eea5140d4373a86fdbc1bbf8a`  
		Last Modified: Wed, 09 Apr 2025 02:21:35 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23a4af428b6c4dbc4cc128aca9a99eb23f3699a73da2a110061364241c6870d`  
		Last Modified: Wed, 09 Apr 2025 02:21:34 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5786ceea932f396b7b6b6fd5ee32570ff63e17601d2c403e6ef1cee80096b008`  
		Last Modified: Wed, 09 Apr 2025 02:21:33 GMT  
		Size: 69.4 KB (69448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731348db8664f722d7ce2d101485080912ab13e1ebbef297299a9f2756efffbf`  
		Last Modified: Wed, 09 Apr 2025 02:21:33 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9a99bdb0fb34dba05738d50396f3519727b8c2199ae588718eb718a9ad3d42`  
		Last Modified: Wed, 09 Apr 2025 02:21:44 GMT  
		Size: 194.6 MB (194553876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd499be6a8dba4f6014d6b8290e0376d4d870d068f7d150c3f21dc5d2ba535c7`  
		Last Modified: Wed, 09 Apr 2025 02:21:34 GMT  
		Size: 108.1 KB (108114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20737ff1e4f620f821f8d8f87416b00663f579418140ca8174cb18f8ac528a3d`  
		Last Modified: Wed, 09 Apr 2025 02:21:34 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
