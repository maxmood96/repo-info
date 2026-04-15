## `eclipse-temurin:26_35-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:eb217e3a093956b7310822ebbc3a95b0c64fe358c5b5106dd15a4ffe2e5d72f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:26_35-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:02cadff8523e9ebb90af81ca2f623d02486a5c8f88f3b88feb14420634722a8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341217395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343c0c791c3af6a3dc7788a1c4875397d8eb021f2a26d9e04c9e3e0e1cc12055`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:14:26 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:14:26 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 14 Apr 2026 22:14:27 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 14 Apr 2026 22:14:27 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:14:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:14:30 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:14:42 GMT
COPY dir:8f93d89558d485d03b81034182d43f2557754598b0731c760b32ca0af365b3c1 in C:\openjdk-26 
# Tue, 14 Apr 2026 22:14:47 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 14 Apr 2026 22:14:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d416eac18eb1d680dc7f0aebeffb463ada9445f5e5f7b8fbe734879b02cac8`  
		Last Modified: Tue, 14 Apr 2026 22:14:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9747fba0774c40e75e8f91a1319f544e2d3a2ce2b0ac53abe8645676cabf7794`  
		Last Modified: Tue, 14 Apr 2026 22:14:54 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2944dfec1bdd2b80b299eac4aa3c79b0245b79a373007ad0ea32845be304220b`  
		Last Modified: Tue, 14 Apr 2026 22:14:54 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34c03e2cddcbf599427a97a9ea741afdd6c8ed8c605667c5b5473ea115ce841`  
		Last Modified: Tue, 14 Apr 2026 22:14:54 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ac82c4b306992e2d102bcd35e0cece544df25625c9601d39ce861146f5e157`  
		Last Modified: Tue, 14 Apr 2026 22:14:52 GMT  
		Size: 72.2 KB (72196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21f2923917c1b07e7d3db3f6553aed09bef3772f80968aed47ce38c2cc72eb8`  
		Last Modified: Tue, 14 Apr 2026 22:14:52 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3244d589eeaa8db9e0a5174139d9962ee6248e7c565213a7a9a4263bd6c281c7`  
		Last Modified: Tue, 14 Apr 2026 22:15:05 GMT  
		Size: 141.3 MB (141307046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc31e5b4b70a1dc91509b183581e8e0262f98c2f7fcfcfc206011ce63697841`  
		Last Modified: Tue, 14 Apr 2026 22:14:52 GMT  
		Size: 114.7 KB (114674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4703c004c652a1b3e4688a5dbf1ca5c785da988a2406d45368365d3a8120c3f9`  
		Last Modified: Tue, 14 Apr 2026 22:14:52 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
