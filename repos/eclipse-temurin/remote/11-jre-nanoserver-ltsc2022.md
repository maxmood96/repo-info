## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1a1dbf4cc0eac49ba275e0724c0d400110c741741ead829175741a99c31bf682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:454aeb876beea7a66ec9e5e701276bdb4f76a549f760db7ed3b1d15537640726
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164024129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5b95a31eb9c408a6fd744cc50dfa3f4c5578e3a72f8bb48178c4c117f41197`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:18:26 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 10 Jul 2024 17:18:26 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Jul 2024 17:18:27 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:18:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:18:36 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:19:16 GMT
COPY dir:b092036da9619d86aad01e40fe92454a038bf12563d3a63208d5f3f51004688a in C:\openjdk-11 
# Wed, 10 Jul 2024 17:19:25 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49db8259042be4df6cd427a4f8d442f29492106caea180a69ab6e573bfede29`  
		Last Modified: Wed, 10 Jul 2024 17:39:35 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcae028b75a0ab4790b64c099f969203447b12bb79e308919e09b019a7d169b`  
		Last Modified: Wed, 10 Jul 2024 17:39:35 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de042bb20d46965d4aa43c5cea3a8d1aebfee8eb9a0bd7a00cc801f72bd12ce`  
		Last Modified: Wed, 10 Jul 2024 17:39:35 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614effc4c5e5f8461be75269c0ff2273b6958fe3364c1b0885c0c581ccbaf708`  
		Last Modified: Wed, 10 Jul 2024 17:39:33 GMT  
		Size: 81.2 KB (81195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dadaa039ffed31184e70603ab50918341815d96581fbeec22d8c5bbecbf0b89`  
		Last Modified: Wed, 10 Jul 2024 17:39:33 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51f694678cd93050385edc31c52d5463bf23678c545b7996aa19fe66ba525c9`  
		Last Modified: Wed, 10 Jul 2024 17:40:03 GMT  
		Size: 43.4 MB (43384369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a60a21497cdb5befc9cda11d496a1dba5b84e3b2002d012bd90f961c146de7`  
		Last Modified: Wed, 10 Jul 2024 17:39:57 GMT  
		Size: 62.5 KB (62491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
