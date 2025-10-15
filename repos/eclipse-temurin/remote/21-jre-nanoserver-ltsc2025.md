## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:ed0cebc3a8f4ae680d08bd5eb0ecb67d4a90c96e0dc03beb75f635373b447f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull eclipse-temurin@sha256:f316c77f32a9356604a6746e48300d505b96b623ab5ff58d00fddd1fd3fbee6f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243202204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946eba09d3bac885574de6903def2cbe0cc5b88eda048b4350bc9376e46283c9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Oct 2025 15:58:41 GMT
RUN Apply image 10.0.26100.6899
# Tue, 14 Oct 2025 21:13:24 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:25 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 14 Oct 2025 21:13:26 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 14 Oct 2025 21:13:27 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:33 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:40 GMT
COPY dir:1d2e38188fefbb829677ed8e6106bab9aec7034078d0a523158404f660841581 in C:\openjdk-21 
# Tue, 14 Oct 2025 21:13:44 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:463edd10ad50b00cf92c69fc3eaa85e1fa40aad1b7938fa232899405bd80f001`  
		Last Modified: Tue, 14 Oct 2025 22:41:48 GMT  
		Size: 194.0 MB (194026741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d590e9d105ec2ff236c7afe562fb5cf3a5b74015f07256c22b45c2c8d1be27`  
		Last Modified: Tue, 14 Oct 2025 21:14:34 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b3533006754baa7ce72df445d0d18c58b9c056b2d5da6b66676d0af952a53c`  
		Last Modified: Tue, 14 Oct 2025 21:14:34 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36a1ef9d731b5392954c7c91a2a895ea95360952d6b48396c1337fcd6fc340d`  
		Last Modified: Tue, 14 Oct 2025 21:14:34 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67d2c94a931d0acaf31c92aaf9d411b63722e6fe1bbe043673e23b1963c92b3`  
		Last Modified: Tue, 14 Oct 2025 21:14:34 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8db4d0662cda51f64678e2d99f9758a30394a931676fdff3f08c09d9bdf0c6`  
		Last Modified: Tue, 14 Oct 2025 21:14:34 GMT  
		Size: 73.2 KB (73198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f6790071016c217903fa2b1cce47572de74e45144a6458d7a13cde15bd2f83`  
		Last Modified: Tue, 14 Oct 2025 21:14:34 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3494c2e428ceb85429cc38145730a5ddc27f092ab420de0acb9e408bffb1d7`  
		Last Modified: Tue, 14 Oct 2025 21:14:38 GMT  
		Size: 49.0 MB (49011198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31922012d94c99de3f68ffd39ee7976c5bb7fa3a275805a9bb328820a016886f`  
		Last Modified: Tue, 14 Oct 2025 21:14:35 GMT  
		Size: 85.7 KB (85727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
