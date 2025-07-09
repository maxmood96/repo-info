## `eclipse-temurin:8u452-b09-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:77bb6145dd2ec1b6742b184f9c6b5df42cc0ff3ece842265e327ca7310ad3900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:8u452-b09-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:3f1ae717a017a250519b8937261ea8c011433a3384ea95cb8e813c86e3673765
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163369761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1970f161fbf7d2c5236cb918f0959e3c266a41ee5881a0eb77bac17737d1f6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:12:42 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:12:43 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 09 Jul 2025 19:12:44 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Jul 2025 19:12:45 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:12:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:12:49 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:12:52 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Wed, 09 Jul 2025 19:12:56 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77606dd0217251d8037bc5b2bf924dbe90559080ee2c9d7d9bfc6412e44aa3d2`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a9c9ac56321c9673b029fe3a2797d91440e63669a4facc63605f0ce860d412`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965e3cfed9b4560b01cd15382c3500521840b5887c1a9efd9f5f44f79c3ce435`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18eaa974dd27b4991a52a60afe84eaf169edc339dada57502d6d7e3db4be7123`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0b1b5a88c751e587e3ca40c9b683cb4ceb533fd369d9af835dd33936da11b`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 78.3 KB (78307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8b8051038fcf281479f5edb3012e901a180336c669d8e925a5e6a0ac18e1ba`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bdc3a970b7ea52bb42f6242df2d7059f89d6b5a21d4f031c6a2ba1a8e013f9`  
		Last Modified: Wed, 09 Jul 2025 19:13:30 GMT  
		Size: 40.6 MB (40553633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d582a9bae4d8f9bd9576c1578acd32ca0a7b908e815e7720a04a4d89511d7add`  
		Last Modified: Wed, 09 Jul 2025 19:13:26 GMT  
		Size: 101.7 KB (101737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
