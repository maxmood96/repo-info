## `eclipse-temurin:8u352-b08-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:95f7ec615a7ec63c61e02edcba937224d05b64ce3470b33461deff5f2030cd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1249; amd64

### `eclipse-temurin:8u352-b08-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:fdc76d68a4ade31b1458e8bd7dd7f394bb12be6960d4323f7f8153172c8a4061
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222746263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b73261c27535851115584aea38d9ffb6549611165b2f2436887bc497222a0d0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 07:21:30 GMT
RUN Apply image 10.0.20348.1249
# Tue, 08 Nov 2022 19:27:23 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 19:27:24 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 08 Nov 2022 19:27:25 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 08 Nov 2022 19:27:25 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 19:27:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 19:27:43 GMT
USER ContainerUser
# Tue, 08 Nov 2022 19:27:54 GMT
COPY dir:3f9950b949d84f617218d6370bf5d9344385a96fee23c5d0245f1523c4ce092b in C:\openjdk-8 
# Tue, 08 Nov 2022 19:28:42 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:72e5d750fe8c1a32d4a26ef3b4a4e1f6124ac079b142f12724af2abfcba1c8b3`  
		Last Modified: Tue, 08 Nov 2022 19:57:58 GMT  
		Size: 122.1 MB (122092167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd83067a7e6c6d9dab3ac0265a21919de95a0bf4e737e647fbf3e43c9874b0`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220e123f23808745fc630305de0ce242cb9a6c565cf4f700e22655ecf005687`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c25f1362ec097d0956355257914a48a3b53f55e8671e01cef2b0e3c09c2da4`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3937de06541d6c6a90657c15b73a603495a8d9f762eef4c868205c91c8dbb15c`  
		Last Modified: Tue, 08 Nov 2022 19:57:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d7087dd3a321a3aacf542b973f32ba8201f01dbb83c2cb89d350df169b7628`  
		Last Modified: Tue, 08 Nov 2022 19:57:25 GMT  
		Size: 79.6 KB (79630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375446a6e44c1ad04d6728e1b203b940f5a24bcbc2be35a789b03c1d5dabfabd`  
		Last Modified: Tue, 08 Nov 2022 19:57:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34772dce1f6b3f9671e813b130936e7c79e286e66ce2cfdc4159942e3bc840ec`  
		Last Modified: Tue, 08 Nov 2022 19:57:42 GMT  
		Size: 100.5 MB (100490566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790437c0068600c1ee6d15d7c04f6a474bfa6393faf17efe6dc51a455cfec718`  
		Last Modified: Tue, 08 Nov 2022 19:57:25 GMT  
		Size: 78.2 KB (78190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
