## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a6b188d6eb498419ec7d2b7c2ccd9e0a0acff4a190fff342b35d0fa4068d86dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull eclipse-temurin@sha256:2b5d900f2cf13b72ca2a473a6bdc1230a93bd3f78072ebb5448ae1781d6b42d4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169438626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56766e08515f8c615439783ab48ec2ddce3077510c9305e49c28aac5b8c75202`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Oct 2023 21:30:39 GMT
RUN Apply image 10.0.20348.2031
# Wed, 11 Oct 2023 02:14:39 GMT
SHELL [cmd /s /c]
# Wed, 11 Oct 2023 17:43:06 GMT
ENV JAVA_VERSION=jdk-21+35
# Wed, 11 Oct 2023 17:43:07 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 11 Oct 2023 17:43:07 GMT
USER ContainerAdministrator
# Wed, 11 Oct 2023 17:43:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Oct 2023 17:43:20 GMT
USER ContainerUser
# Wed, 11 Oct 2023 17:44:06 GMT
COPY dir:5d7e2a5825eef6d21094c71010e496d2276d2a39ff1ed82cc9374a1e7bd17e0b in C:\openjdk-21 
# Wed, 11 Oct 2023 17:44:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fff54800e03713ba81736f43d985319592fc643a1a32b62dbd5c0ec36549de00`  
		Last Modified: Tue, 10 Oct 2023 17:30:43 GMT  
		Size: 120.6 MB (120604344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142fccf33f15e2c503ce4023e2e496d7a99bd036e8b83264772e9dab49c325b3`  
		Last Modified: Wed, 11 Oct 2023 07:29:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db759a0d2eb850278fdc67873394befb94c0bc7ff4a5b1b0bbbb904d91407a5`  
		Last Modified: Wed, 11 Oct 2023 17:49:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedcf5383f0db1557f46c8a53c50a5eaa73db88554d20ef9a0bdb134715a8e6a`  
		Last Modified: Wed, 11 Oct 2023 17:49:57 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eab2b4ae29c36715aa3adcd2e504e70a9a18bce55b74bcd508feaa05655938e`  
		Last Modified: Wed, 11 Oct 2023 17:49:57 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40dd4bbe4acd4654b64c1772fea5a9f91ad011b907a900680eac66716fb57520`  
		Last Modified: Wed, 11 Oct 2023 17:49:55 GMT  
		Size: 79.4 KB (79402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e2889dbf7434503d2db34e6a35a2dac63167016c2d6d771affaa80238ef2b2`  
		Last Modified: Wed, 11 Oct 2023 17:49:55 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf63a19823c74552a30f801865976482c29c23a2b0dbbcc36593e2fad64e24f`  
		Last Modified: Wed, 11 Oct 2023 17:50:38 GMT  
		Size: 48.7 MB (48687927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc64c40eb2174a9b0760079debee2b16c5b7e21cb352c43d578938f701d713f9`  
		Last Modified: Wed, 11 Oct 2023 17:50:29 GMT  
		Size: 61.1 KB (61106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
