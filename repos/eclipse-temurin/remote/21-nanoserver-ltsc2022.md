## `eclipse-temurin:21-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ffc93f36331d4a30f276bbc6514612e85ecb1cc83dd74423c01a8d2467ecac53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:21-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:3fa098f8e9cbd9db4f63beff17b8db60f0dee138dfa992c46028a15ff7147abf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.1 MB (329108473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35d640f9532b8264d9802de5eec29c4f9dbe5fb784b911d795a6c9e7ffe1104`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:39 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:24:38 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 13 May 2026 00:24:38 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 13 May 2026 00:24:38 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:24:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:24:40 GMT
USER ContainerUser
# Wed, 13 May 2026 00:24:48 GMT
COPY dir:be4fce80d476aa164b4bdafca77eddb646da4c27d929101014e2067a583f974e in C:\openjdk-21 
# Wed, 13 May 2026 00:24:54 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 May 2026 00:24:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60ed370d326231e88b53b9eb83b5e7c2a02f147b495f0751da4e9072d5d7a91`  
		Last Modified: Wed, 13 May 2026 00:23:57 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d26628cd2eb72d3d84e9013d08cd50adee081f0fe988c2e3b3f0c2672f8d70b`  
		Last Modified: Wed, 13 May 2026 00:24:59 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7efeb7ef5a010d14b572d8c37f1c896d67d879540e32f63d89b2e8d4fb2f46`  
		Last Modified: Wed, 13 May 2026 00:25:00 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26541c4b87cf6cd752644ffc2c5f99c7697a01c97d9acff2b19114593ae3af3`  
		Last Modified: Wed, 13 May 2026 00:24:59 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddbdf2ffd9bee9dca81f43938845dcb4af4d2f47ed65279390823d973361b05`  
		Last Modified: Wed, 13 May 2026 00:24:58 GMT  
		Size: 77.5 KB (77528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a077e04e1f65ab0c1fa951f19316c7f3c842f244c8651cbf096ba0393daf6de`  
		Last Modified: Wed, 13 May 2026 00:24:58 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae80faea77e1ee233aba063a8b43b042846a59a1dc47e2f0a4bd71c67158469`  
		Last Modified: Wed, 13 May 2026 00:25:11 GMT  
		Size: 201.9 MB (201874389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776c728d2950ac9d54a33c802a3f907b5df4e504ac573cfe74552091d240c5b1`  
		Last Modified: Wed, 13 May 2026 00:24:58 GMT  
		Size: 111.4 KB (111443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85192535cd90baa5ffa58da7fb0050ea8cb058a5a1d16fa587f023d0c1e509d0`  
		Last Modified: Wed, 13 May 2026 00:24:58 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
