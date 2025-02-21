## `eclipse-temurin:8-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b5a430ad652a31a906506fa5803fa28dc0281607f7366efe96eb8c4b0250c930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:8-nanoserver-1809` - windows version 10.0.17763.6893; amd64

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
