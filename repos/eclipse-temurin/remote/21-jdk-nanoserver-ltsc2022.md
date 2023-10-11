## `eclipse-temurin:21-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:dd7c24f683e4303430c1559c97a39b73c90a188703647abbf3c86d4becf14156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull eclipse-temurin@sha256:5b4806758cb9632b36dbda2421e99c6bcb75c4a762990139b1f1f4ac54ef3ae9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320909153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9618a3cd0bfc0bb8a73db8a620240401d7b79b51d76c2e7292a5ccc074cfa7`
-	Default Command: `["jshell"]`
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
# Wed, 11 Oct 2023 17:43:36 GMT
COPY dir:f06f5ee7db845501c8fe05855f9c29461cda8cefd674e3441d48367166fadd37 in C:\openjdk-21 
# Wed, 11 Oct 2023 17:43:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Oct 2023 17:43:49 GMT
CMD ["jshell"]
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
	-	`sha256:e36a787f29e7a9d20a296e4fd9d5ae10ba202047ebbc8b9de50eabcbb751eba7`  
		Last Modified: Wed, 11 Oct 2023 17:50:15 GMT  
		Size: 200.2 MB (200157326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978c728c3c244d09c2d449d0109848b76fc2234cc967122eb4c8249f502016e5`  
		Last Modified: Wed, 11 Oct 2023 17:49:55 GMT  
		Size: 61.1 KB (61073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d28a983f1abff5bc2565c8519908a52412afe40b001ea88d827905d814fd9`  
		Last Modified: Wed, 11 Oct 2023 17:49:55 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
