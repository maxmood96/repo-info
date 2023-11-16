## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:5fb8ca64a7d4e0af53b6f2a32af46b5a1962cb4a9a6b7c54557706a4b4408fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull eclipse-temurin@sha256:0d0801c12c3b870b20dd059ac40e8e88b366a45bb6d037a4237d53b701b5a053
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206322908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bd167f85efa60aa4d5828973201a10cc3fd6deb246db9e37cb398819aff2c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 01:41:12 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 01:41:13 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Thu, 16 Nov 2023 01:41:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 16 Nov 2023 01:41:15 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 01:41:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 01:41:27 GMT
USER ContainerUser
# Thu, 16 Nov 2023 01:41:39 GMT
COPY dir:d9c44d909d2b41aad5bf6fa4f7c7d36e81063822ae5e7ef30e4851bbe7809503 in C:\openjdk-8 
# Thu, 16 Nov 2023 01:42:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5c133738aab79d4c21c47e77cb838e2d00166f5e3e2632177622f67488259`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001b8d65ec89d4fd832acce6037db85dddec1200131f5e609fa4a8c74d9aa08d`  
		Last Modified: Thu, 16 Nov 2023 02:28:07 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098df4d2a628a16ff447f34741e7530283c13e252104d9e3ac749df571941064`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79510d2c134c91689203a24e81971d573b835fdd61baedd442def46468cd6b3d`  
		Last Modified: Thu, 16 Nov 2023 02:28:06 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ee22aa6b0b0623853f8dd73c8d7db27ef87fc407914c74e6b377815e6b5441`  
		Last Modified: Thu, 16 Nov 2023 02:28:06 GMT  
		Size: 69.1 KB (69126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0405951c92e8acd1a52ba508748bbbb67cbf3f9a60ac58872953b1640d32447a`  
		Last Modified: Thu, 16 Nov 2023 02:28:06 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24767bba8f15bf1cc90303469df84e3e903976774417ab6b3a741c3a247ddc33`  
		Last Modified: Thu, 16 Nov 2023 02:28:19 GMT  
		Size: 101.7 MB (101669776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172f19b676689d2dc1d4be2af596ef5edb4736e3e2f12a809b6de2b9afcbd2c1`  
		Last Modified: Thu, 16 Nov 2023 02:28:06 GMT  
		Size: 81.3 KB (81285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
