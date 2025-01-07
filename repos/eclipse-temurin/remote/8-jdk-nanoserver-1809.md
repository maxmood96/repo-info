## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:4957d5286206633771ca3c8c0c9380caa1fb73c291fc88b9de72a383e392e196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull eclipse-temurin@sha256:8e8bf33b6e49f941ad6bed355461bbb820823f1c3ff0678122b03216540871ed
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258880337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237e4102c402af697c66b4ec96587c17b2c7a4afffd8ad3de69ea2d00352f794`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:49:43 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:49:45 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 11 Dec 2024 21:49:46 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Dec 2024 21:49:46 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:49:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:49:49 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:49:55 GMT
COPY dir:20063c61efcf25f5137b7902f122f09a78eae5d617f3f56a66aed8780998122b in C:\openjdk-8 
# Wed, 11 Dec 2024 21:49:59 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b8ec5a38f4b03a35328c43abb079aa031ea01d60dc4069d3878917a3d9ed48`  
		Last Modified: Wed, 11 Dec 2024 21:50:03 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77eb3d0db7f9039cb8ae1e9cb25941f588f6eeb41b04ecd7dbe45aba74e77e8`  
		Last Modified: Wed, 11 Dec 2024 21:50:03 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfb765ef0d1da3214278cd3d2c1ac34ea03c10d7021aee2d7075921f7a08466`  
		Last Modified: Wed, 11 Dec 2024 21:50:03 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585b67105d7ca657523ed4b4de9fb1a8ec198e4cc2931932d5a30df0b4354bea`  
		Last Modified: Wed, 11 Dec 2024 21:50:02 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b77162570d94bc8739231b3861bc2ec3f31d81357aac58016fcf4b033779e`  
		Size: 74.3 KB (74253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0633ef6b6eb2009fae909cbda7c9cbae70f1538ca5e2c423ed81de017bb48c79`  
		Last Modified: Wed, 11 Dec 2024 21:50:02 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa434e33816597a69964e7b23f91ec6fa85da4d0bfbf0910a494b011b3c137f6`  
		Last Modified: Wed, 11 Dec 2024 21:50:09 GMT  
		Size: 103.4 MB (103442740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19888b6170f84bc1dec17049de0cd909e21107180bcea133892917023b9607`  
		Last Modified: Wed, 11 Dec 2024 21:50:02 GMT  
		Size: 126.2 KB (126220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
