## `eclipse-temurin:21-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9779a269e2e29e81c8f01a9a6ad821f16f8d09ac87470f4836ace91bc3610ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:21-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:b79e8e427b242672463a6df14118c02bac12a84d07686969a44f92b01f1558e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.1 MB (326095840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d0c36e13b072c1e49c60d60485466c1f6199c0f0ef3832e5eb54f5f6b00161`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:28 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:22:10 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 09 Jun 2026 23:22:10 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 09 Jun 2026 23:22:11 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:22:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:22:14 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:22:43 GMT
COPY dir:be4fce80d476aa164b4bdafca77eddb646da4c27d929101014e2067a583f974e in C:\openjdk-21 
# Tue, 09 Jun 2026 23:22:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Jun 2026 23:22:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574a0be87f6c25e257370163ca662e1efb19ea531635bc6e86aca63b32da7e65`  
		Last Modified: Tue, 09 Jun 2026 23:21:02 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661bceb8ffec8566834358527dfb793cc33d66402a9ff06ff62cf2501a4e3cae`  
		Last Modified: Tue, 09 Jun 2026 23:22:55 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46622d76f1c02aff4faa106fba06156ac8477b67db8a4f3d587e747dcf552025`  
		Last Modified: Tue, 09 Jun 2026 23:22:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2eb58d77ec0c884445fbba95bfd22735bdfe71fe53e9ea8300c1b3026b55f2c`  
		Last Modified: Tue, 09 Jun 2026 23:22:55 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77115b5b30784c93a0e6ff0bbea71e19e329c924e0147c610d0e1e7beb60e7a8`  
		Last Modified: Tue, 09 Jun 2026 23:22:53 GMT  
		Size: 75.4 KB (75449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62183781d6f832eb819bbb3bf08de83b0ab956b843359edc4f70b3de29249955`  
		Last Modified: Tue, 09 Jun 2026 23:22:53 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c2b3ad4a83839fb2b1b352306af4ac016ee1dfeea6827a516e695db8562912`  
		Last Modified: Tue, 09 Jun 2026 23:23:07 GMT  
		Size: 201.9 MB (201875349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8732ebaa98be053cef507f9812254de9a4f22074e83cd3ed3a29cecc096760ef`  
		Last Modified: Tue, 09 Jun 2026 23:22:53 GMT  
		Size: 141.2 KB (141178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d22cfeb15a1c6c5778752749bf7badd0e47ff729957a9ace4b66d35e0224a2`  
		Last Modified: Tue, 09 Jun 2026 23:22:53 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
