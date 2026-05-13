## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b55aedd756bb8351e831948d3568c90f51c7f8d679aad039d59a4d6d90f9e0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:45c16750382267742a636199313deef71db270fd45458f94ea28009b6c3866a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314852068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e20f42e71b31a604e8272a6c02e7b00774f6700cb0ad78b925446b042daa2b0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:32 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:24:26 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Wed, 13 May 2026 00:24:27 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 May 2026 00:24:27 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:24:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:24:29 GMT
USER ContainerUser
# Wed, 13 May 2026 00:24:35 GMT
COPY dir:efa343062fcab6068fd499c77aea77fee33bf19a70fc27fbcf8f5891917744d1 in C:\openjdk-17 
# Wed, 13 May 2026 00:24:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 May 2026 00:24:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03cbcd303d3a3d248ab22d617e183ed76d01abedfee5c52cc9fb7f6a87170f0`  
		Last Modified: Wed, 13 May 2026 00:23:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9743b6e5d13d29678e1c531df2f76d5b17e37919fbfd1d8c80a40fc96a13a782`  
		Last Modified: Wed, 13 May 2026 00:24:47 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2092ec2b4b15022fba8eea123bf01e5962c031cc7d36bec91419361e10e772`  
		Last Modified: Wed, 13 May 2026 00:24:47 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1beb8e8c2bfbe8f47011cbc2c09561501d64863ec95885fe58ce23ef9847732d`  
		Last Modified: Wed, 13 May 2026 00:24:46 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511574e445367ddb50cfb4496b500e7618724fbfab2a7cfeb39a2f25702ccc5b`  
		Last Modified: Wed, 13 May 2026 00:24:45 GMT  
		Size: 78.0 KB (77971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6eff006c7c0e2f5f52b7173c9a371634ea8d9c55bc461f7d67618d9d05aaee0`  
		Last Modified: Wed, 13 May 2026 00:24:45 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7d776f5324ab2cae60b740166d3a9370d4643e7fe6cb651f6391ce267ebf69`  
		Last Modified: Wed, 13 May 2026 00:24:56 GMT  
		Size: 187.6 MB (187621723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff1a5ce9e80d001610afb04d37f6a617f1eb2e7b11a05dae5c03dd070f4ac97`  
		Last Modified: Wed, 13 May 2026 00:24:45 GMT  
		Size: 107.3 KB (107283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbbad840437f009664c21d7e3d9734c2b84c5869155cfd532bcb227aa1e8cef`  
		Last Modified: Wed, 13 May 2026 00:24:45 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
