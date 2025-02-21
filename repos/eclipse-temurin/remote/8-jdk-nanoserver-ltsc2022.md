## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3884da58a392a901d2a54bb468cb1780a4230997997425976c775da9f99de8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:c9331b1da34d87fac37fd70466903880071bcd6dee037766f6949f3524492988
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223288288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3fe8f5e067838e335a369177ad64254fe840d9ab1b4c26f564c2fa57648465`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:21:33 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:21:34 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 13 Feb 2025 01:21:35 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 13 Feb 2025 01:21:35 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:21:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:21:39 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:21:45 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Thu, 13 Feb 2025 01:21:49 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349c13f249e526579c97b00b21fbb16e18a0a41a94a7f31fcf6290bd50cf7bf2`  
		Last Modified: Thu, 13 Feb 2025 01:21:55 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aba42fb9e5f066dcd98949008cbc4f54344e885ea2d228e47dd6ea27d509ca9`  
		Last Modified: Thu, 13 Feb 2025 01:21:55 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f57176b6761353cadc2a8984ffc26f876666abb9c5937d638e39876fedd575`  
		Last Modified: Thu, 13 Feb 2025 01:21:55 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb28198f8611d90099035bb5669a3fdad3587c06a969c5b52dede2c145047674`  
		Last Modified: Thu, 13 Feb 2025 01:21:53 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5dbf094132e4796e49d038816fd1b55d83c94fed4196b2247b75b9b6b70410`  
		Last Modified: Thu, 13 Feb 2025 01:21:53 GMT  
		Size: 78.0 KB (78008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c4c9e8f5dd2ca1e1824224832dfc541cacb6981e7d4db9a2c607df1c47aca4`  
		Last Modified: Thu, 13 Feb 2025 01:21:53 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff88ede46a6cab00355e65e32075f77a61694767e5f14f5633081f9015a9aef`  
		Last Modified: Thu, 13 Feb 2025 01:22:00 GMT  
		Size: 102.4 MB (102431271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081e40403ad64992d30c0fd82f1e8e752fdfcb1decf36f175e78c0c94b1fa28e`  
		Last Modified: Thu, 13 Feb 2025 01:21:53 GMT  
		Size: 107.1 KB (107107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
