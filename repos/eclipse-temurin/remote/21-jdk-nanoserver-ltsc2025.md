## `eclipse-temurin:21-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:7aae6876fbb82b911559f68dbfb454c62170a417aadd4dd12f1fac42f22fc538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull eclipse-temurin@sha256:e778580a0e8857e80bef1bde8a2c25141d18876e441f01eef34bdce5d0a5cbee
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 MB (395878142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a83443bc64047a5a802df7bd8b20c963a54429bb61fe9bab6ee789dadf96897`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Oct 2025 15:58:41 GMT
RUN Apply image 10.0.26100.6899
# Tue, 14 Oct 2025 21:13:39 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:39 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 14 Oct 2025 21:13:39 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 14 Oct 2025 21:13:40 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:44 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:52 GMT
COPY dir:a3fe1d88014e165c39b52565bb4587e5a787fc090e6660a0edced9167c6512ac in C:\openjdk-21 
# Tue, 14 Oct 2025 21:13:57 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 14 Oct 2025 21:13:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:463edd10ad50b00cf92c69fc3eaa85e1fa40aad1b7938fa232899405bd80f001`  
		Last Modified: Tue, 14 Oct 2025 22:41:48 GMT  
		Size: 194.0 MB (194026741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c714c0b8be205d316860e805ce9e1c816c35d866c460b278194574124174ae1`  
		Last Modified: Tue, 14 Oct 2025 21:14:39 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd6e5d3bbba4d3e27a8dc1edbe47042fd3c4eb953f12a766071217eaad1d1a4`  
		Last Modified: Tue, 14 Oct 2025 21:14:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc15d813d429bf216223caaf7c8d0682b462b997de4df1a90823ca189032284`  
		Last Modified: Tue, 14 Oct 2025 21:14:39 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bcba0e1267cf8d221714da75420d5e7ef72f050726d22396d318146b214c94`  
		Last Modified: Tue, 14 Oct 2025 21:14:39 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369c1c0de52135d257575507d2854d68e0cfb4e2e55c696aa841f5ff84baaf95`  
		Last Modified: Tue, 14 Oct 2025 21:14:38 GMT  
		Size: 70.6 KB (70629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ae03462c2a1fab5a560043ecf91ccfb9bad7534e3a18761172df25fcbcc312`  
		Last Modified: Tue, 14 Oct 2025 21:14:39 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c53be046dbda1f6828a06d5f3761db0a8461a6076eb28e414af6d36d7ba933`  
		Last Modified: Wed, 15 Oct 2025 00:16:38 GMT  
		Size: 201.7 MB (201671976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7c6000104f39fa382276340314aa286b0e5ed8bb76a6b4f8200d0747aa28db`  
		Last Modified: Tue, 14 Oct 2025 21:14:39 GMT  
		Size: 102.4 KB (102381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63a91512c2e97c36280867d5c88a05bbcbb0c129bbe821952fec89c68d52829`  
		Last Modified: Tue, 14 Oct 2025 21:14:38 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
