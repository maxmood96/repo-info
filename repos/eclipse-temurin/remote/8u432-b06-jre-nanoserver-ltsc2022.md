## `eclipse-temurin:8u432-b06-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:f7babee52e381d3e73f7f324fcbb850800080262cd7ead54c1b2df3cdd4b8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:8u432-b06-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:63317c5111edc7c6461cda7ad2a8dbd63d9743fa2dffe5d4449ccf40a262726e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.8 MB (161758975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337fdaf38d43e74f38d4eda3df7c372fbb20aebb922059371e48cd3d653e8f67`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 24 Oct 2024 01:53:01 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:53:02 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 24 Oct 2024 01:53:02 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 24 Oct 2024 01:53:03 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:29 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:33 GMT
COPY dir:47bf2d2ef237403b98ba2f50909368ef2c147e2a609dd71db23cc690a276ad54 in C:\openjdk-8 
# Thu, 24 Oct 2024 01:53:38 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9006cd878565e0783ea9060f882cc0ac70de8b44dd222e305a62cf0fae50d3`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9bdf0a336432b3903ba9511e55bb935cb8cbc07b86302ec53e0eecd46ed75f`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3c647f3744dceac40e6f3c98a46e6e1345489c0b538b5aab11f04d93d12137`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dee900e924768e915861529ad1db38905d6646457949017f6695657061cc4d`  
		Last Modified: Thu, 24 Oct 2024 01:53:40 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1de77e69b62e8669ccfa6bc6f26a211bf754873acdd2a489d559dfd461cfba`  
		Last Modified: Thu, 24 Oct 2024 01:53:40 GMT  
		Size: 88.4 KB (88388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee4616a1b70fbf09fac352bf1986f2be2bd841d5679a4d06c7746ea63029922`  
		Last Modified: Thu, 24 Oct 2024 01:53:40 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01d76b20c71e76a3bf6939e0b15298ff2db9178ad53df36656ecfdd80d9144f`  
		Last Modified: Thu, 24 Oct 2024 01:53:43 GMT  
		Size: 41.1 MB (41060644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becb3e8bc76700142631198f3d440a69dcbdfda14839a5995498733323b2a9b8`  
		Last Modified: Thu, 24 Oct 2024 01:53:40 GMT  
		Size: 93.8 KB (93754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
