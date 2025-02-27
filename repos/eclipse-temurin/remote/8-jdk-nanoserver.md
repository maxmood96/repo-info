## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0b2974c6200b6cd6abcb6d38516cc8f5dc675ae36c014db7a38e5faca81880bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.3207; amd64

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

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:ad1b05c1ea86680df53038263b19b97c1cb2073918c81a92f3e3133f8112b0fe
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209561415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7687a3b90a82b9ea684b8b955f3fc8f6fec8799458345a6c17de5ba939644c08`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:16:43 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:16:45 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 13 Feb 2025 01:16:46 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 13 Feb 2025 01:16:46 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:16:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:16:49 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:16:54 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Thu, 13 Feb 2025 01:16:59 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1591a73ef1bcff031aee649f6cc6aeff83d898971ff92a102f0c04be184561b7`  
		Last Modified: Thu, 13 Feb 2025 01:17:03 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1f49ca71af382c36da1043b5ea990b48e908bde4097cddb2e44d83d3ea638a`  
		Last Modified: Thu, 13 Feb 2025 01:17:03 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfdc08e438261c0de3538d5cde9e5ed40741e4f1ecc39978d6a457cbe719321`  
		Last Modified: Thu, 13 Feb 2025 01:17:03 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b4178f999d2306a3bbe9ae68f648951ed4b58a77781c6a51c513d2f933c2d6`  
		Last Modified: Thu, 13 Feb 2025 01:17:02 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adab557f3886603fcc4797dcbc9fc0860dca35fd5a0804a6132dfabe36f14fea`  
		Last Modified: Thu, 13 Feb 2025 01:17:02 GMT  
		Size: 84.0 KB (84027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7804df8ceec7850cb3547c2d20d1873f2ad4424cda5e49285ca09c750b3b211b`  
		Last Modified: Thu, 13 Feb 2025 01:17:02 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fb228f61015f155b63886506c10736b1ac9e033e84b9e9634b1ef5f8b22166`  
		Last Modified: Thu, 13 Feb 2025 01:17:08 GMT  
		Size: 102.4 MB (102431206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a3eec2fcf8effb53b88d266c1dac7f5bbb0d63c5def9410b892ba338ddf478`  
		Last Modified: Thu, 13 Feb 2025 01:17:02 GMT  
		Size: 125.5 KB (125516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
