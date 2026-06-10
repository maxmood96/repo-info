## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:fbf0cf7f34c4bad3af4a0e1323d1aa5688f19a60a7e1f399e4bfbfb14d651bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:17b4ea3e174f59185f9dfb33747842b43ca8e1b9d9837908df1900dc195cfdc7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311851132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bd8c38f30135f4fef572d387b9bc05e6d6e505d78f621334148641b9333b52`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:22:03 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:22:03 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 09 Jun 2026 23:22:04 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 09 Jun 2026 23:22:04 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:22:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:22:08 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:22:27 GMT
COPY dir:efa343062fcab6068fd499c77aea77fee33bf19a70fc27fbcf8f5891917744d1 in C:\openjdk-17 
# Tue, 09 Jun 2026 23:22:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Jun 2026 23:22:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21034a36b984b051c6068965f6f85374ed184f539d2884326874b78b1347024d`  
		Last Modified: Tue, 09 Jun 2026 23:22:40 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d798c456d9153dbfeeed17b742b6e61a1f05d67d98e7a974203f6e68927f9e8`  
		Last Modified: Tue, 09 Jun 2026 23:22:40 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962407f1b906c1171d7a368ab7b966c681b483c98183c6d8952c3f3e40bb4ce6`  
		Last Modified: Tue, 09 Jun 2026 23:22:40 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47874136e5bd1c6929e5b7cb9e28102d77cde3c2b31acbd01c95683029b4fbcc`  
		Last Modified: Tue, 09 Jun 2026 23:22:40 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f7455bfaba1f7c4c3f430489f5cedd31534795e7c9ce9010c2019dbdd4cc44`  
		Last Modified: Tue, 09 Jun 2026 23:22:38 GMT  
		Size: 88.8 KB (88811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184f57971f99a4fbdcaf3891354c2cae6cf16d2056a4c04914dbd724bd5e574d`  
		Last Modified: Tue, 09 Jun 2026 23:22:38 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1521b5fe5a92b336f6b9eb1a50bdd079c1bc46b3963a81ba74da16fbbdbb728b`  
		Last Modified: Tue, 09 Jun 2026 23:22:51 GMT  
		Size: 187.6 MB (187622158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c18a78dc158bbe3abf49b69c32df4c62fcc46ca7844bf31fd4c2e002442b40f`  
		Last Modified: Tue, 09 Jun 2026 23:22:38 GMT  
		Size: 136.3 KB (136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f542f505f690f2efcd3ebd125ae8f2b5a8cfabbbb6b60d37eb00568873000570`  
		Last Modified: Tue, 09 Jun 2026 23:22:38 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
