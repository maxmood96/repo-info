## `openjdk:11-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:df2ba2304cc819cb1f92230123501bbc28a22c4f8f18ff6b1f0c9ceb059d0d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:11-jre-nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:c321930ec17c42f0a2ebf6e726ebde29bcf4804fd63142cc77e2f60444af9aec
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141827048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8514094c0ac60c85821ca717d19c0cf4e91a4f2a944cdba36171742b2ef06b63`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 19 Jan 2022 22:25:45 GMT
SHELL [cmd /s /c]
# Wed, 19 Jan 2022 22:35:23 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 19 Jan 2022 22:35:24 GMT
USER ContainerAdministrator
# Wed, 19 Jan 2022 22:35:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 19 Jan 2022 22:35:33 GMT
USER ContainerUser
# Thu, 03 Feb 2022 20:19:29 GMT
ENV JAVA_VERSION=11.0.14
# Thu, 03 Feb 2022 20:23:26 GMT
COPY dir:cfebfad0723a0ff7cb715c8613c7ff95f5bc09dd8224aed2718d72001e95ccca in C:\openjdk-11 
# Thu, 03 Feb 2022 20:23:51 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version 	&& echo Complete.
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a1b3e13bb7b3d4b61b5f49a91d6eb9bfcf5539ab89c3687d608f17713c2409b5`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b46917062cd0d7f4c89c1b50441650b2ac0f83c61a58941b641e92b5252e2c`  
		Last Modified: Thu, 20 Jan 2022 02:33:51 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d000e90631a186e004110abc4ac959d5de914a16598f08bed601130c0c9d8b5`  
		Last Modified: Thu, 20 Jan 2022 02:33:50 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f12cf94a966fe4ae61e112d47daf3f720d53758f98395623364d4aebbc887c6`  
		Last Modified: Thu, 20 Jan 2022 02:33:51 GMT  
		Size: 76.5 KB (76519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993db4a377f7c9708998d33ec26ed7ddaf8a082b5e05266399e1ec83d7ef4ca6`  
		Last Modified: Thu, 20 Jan 2022 02:33:48 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4742af10b3bf63a40ed5c74611f584fe8cc2f43d815789d36a7d83624ab1a0e9`  
		Last Modified: Thu, 03 Feb 2022 21:24:58 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077ac332a5c60469cf9c2f5f9c41d8f7cd746b405abf43ef0a03fadb7ce9a848`  
		Last Modified: Thu, 03 Feb 2022 21:26:58 GMT  
		Size: 38.6 MB (38642453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaba5ffec25e0aa29d4919148d33727a735b62174672ef5f4cc2e1b5f07f1e6c`  
		Last Modified: Thu, 03 Feb 2022 21:26:18 GMT  
		Size: 55.9 KB (55868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
