## `eclipse-temurin:8u442-b06-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0e89e57ebdc63cddc4b613a50390aec08ec43a3c47c549719279d7e669054c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:8u442-b06-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:9d7c78b13e53de38a1a3470a1145fc4739ad5736820312fa3873155fa18b75e2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223318394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6386cbef56e66fb82b7e0d67db870141d383f63ecc6c704acdd8776b5b805b30`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:19:35 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:19:36 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 19:19:37 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Mar 2025 19:19:37 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:19:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:19:40 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:19:45 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Wed, 12 Mar 2025 19:19:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a7eb22c346b2739fb13ce46a21f5aba2d795f94dc4eacf060c05eff6f47788`  
		Last Modified: Wed, 12 Mar 2025 19:19:56 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca8dd253d5299e9552267033847d6fbea0864a654ec4a2f6e5b4cd8ff1d41ad`  
		Last Modified: Wed, 12 Mar 2025 19:19:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bce45b12140ad0afdb7c56552dfdb4eb3b458ad9ce740cdd7cffa23f73af560`  
		Last Modified: Wed, 12 Mar 2025 19:19:56 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d2976cec768d9d94b5421d6bca98814d5754c8d0ac475186fe5901ebd8a586`  
		Last Modified: Wed, 12 Mar 2025 19:19:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0ae1817290ada447a19e7116fb3cc598752d8cbdc904d4c457c73eb97fee8b`  
		Last Modified: Wed, 12 Mar 2025 19:19:54 GMT  
		Size: 78.5 KB (78548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e6217011485bb88798884a9bb588bab1d82bd60c750dfe80e28a83714ef9ef`  
		Last Modified: Wed, 12 Mar 2025 19:19:54 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79005d2aa9e6e54f96ae89f524b18a89d4e4360f7ba910e1822b7a3e9858c551`  
		Last Modified: Wed, 12 Mar 2025 19:20:00 GMT  
		Size: 102.4 MB (102432219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f5358eec207990a73202236341a537d204a17d62b543038da71fe04aa1a7ce`  
		Last Modified: Wed, 12 Mar 2025 19:19:54 GMT  
		Size: 106.9 KB (106924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
