## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8944bd734575500196e7f2064901ad94079d4c2da71f669fdc4bfbcac31e7426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:d707a7c0f1099d044495ab33c010ebecbd2517e4faf1fcb7fb166991e67e986a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387522829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aed3b52755d8bed2a33adef9c67ca27bf38fdcd9665dbe0565c9c001bf54d4f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:28:55 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:28:56 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Wed, 13 May 2026 00:28:56 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 May 2026 00:28:57 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:29:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:29:00 GMT
USER ContainerUser
# Wed, 13 May 2026 00:29:12 GMT
COPY dir:efa343062fcab6068fd499c77aea77fee33bf19a70fc27fbcf8f5891917744d1 in C:\openjdk-17 
# Wed, 13 May 2026 00:29:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 May 2026 00:29:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014c40faf0b340885a4bc9a9bb244d9376a40c63e7d9681861a76438ed1baf25`  
		Last Modified: Wed, 13 May 2026 00:29:23 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4066354986761ebc03806d95e0fc8a1056fbdd8f739f1f6f7016c9b63cb4cb63`  
		Last Modified: Wed, 13 May 2026 00:29:23 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d864612d8f95bdc3f981227ef42a86064222826528ffc09db18931860aea70`  
		Last Modified: Wed, 13 May 2026 00:29:23 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f47e54a4a25622a63934a0fbce09f5f80e3215bcd25a695f06f7eb002accd4`  
		Last Modified: Wed, 13 May 2026 00:29:23 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159e92b9ec6da046ac60a1be5be7eaae81845d3a8237e3c6e2bb035192919366`  
		Last Modified: Wed, 13 May 2026 00:29:22 GMT  
		Size: 70.4 KB (70405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f60271094af17e9fb48ac1ef9c01902b2f9712e1aeb72b41cbbb3076b20426`  
		Last Modified: Wed, 13 May 2026 00:29:21 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9196d1dcb6e1b660f874879dc20047a37a105f92cec3df945e039d9ec2073e92`  
		Last Modified: Wed, 13 May 2026 00:29:34 GMT  
		Size: 187.6 MB (187622025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cec6538b3e759ad3f419912d1451536d088c1f82ec06c7af5e266aaeaf569a`  
		Last Modified: Wed, 13 May 2026 00:29:21 GMT  
		Size: 85.0 KB (84972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252d0ce5c08e07c519ed5ebe0917e1df3e5a660f1f1f3aef21ab45c6119661b4`  
		Last Modified: Wed, 13 May 2026 00:29:21 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-nanoserver` - windows version 10.0.20348.5139; amd64

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
