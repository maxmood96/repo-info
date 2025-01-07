## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:db426523a645f64600e7c95457430fa7c33cee90a0fc1fd3f6940d51dcc11b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:7f098c631a5b4735dcc47b7534a66e656e048a20eb29ad2ee8e1d761d8eba9b6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224232484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0955247edd2bfd1ca7dca143adbbdc89490aee01d4fac83a4dba085b5daa34`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:52:20 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:52:20 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 11 Dec 2024 21:52:21 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Dec 2024 21:52:22 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:52:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:52:25 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:52:30 GMT
COPY dir:20063c61efcf25f5137b7902f122f09a78eae5d617f3f56a66aed8780998122b in C:\openjdk-8 
# Wed, 11 Dec 2024 21:52:34 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f1a8494636dfaee9334b074df85b2cfa0518754e22a0bac7f4ff24e5f7df2`  
		Last Modified: Wed, 11 Dec 2024 21:52:38 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c744901f79aee2ab0e4046dfb077c5e62a7ffff91f8942133d07e8404f99019f`  
		Last Modified: Wed, 11 Dec 2024 21:52:38 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd0f7ef31ef1ca957435602940baecff21ca228ba225c1fd6ae53682f1b7d4c`  
		Last Modified: Wed, 11 Dec 2024 21:52:38 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1311de039e97644efb4511f3fb7b489f7ec2d443940dbd9fd343c89ba778147`  
		Last Modified: Wed, 11 Dec 2024 21:52:37 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3696024c1511353fb5b09e690484b90be731298ca51213102a96f2cc529234c4`  
		Last Modified: Wed, 11 Dec 2024 21:52:37 GMT  
		Size: 78.3 KB (78275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8992290c525664c73ea30f1986873a9ae697a4146e2b88ae4f79119f60ae36`  
		Last Modified: Wed, 11 Dec 2024 21:52:37 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfeb02a2fda80195bf25e25e45a1fed25be46f4ddfef0cba8d209987c17b8c`  
		Last Modified: Wed, 11 Dec 2024 21:52:43 GMT  
		Size: 103.4 MB (103441041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194221b962203fdbd2fd274224b8d5d793574975e17f0e68a8989215c7707dfb`  
		Last Modified: Wed, 11 Dec 2024 21:52:37 GMT  
		Size: 106.7 KB (106665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.17763.6659; amd64

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
		Last Modified: Wed, 11 Dec 2024 21:50:02 GMT  
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
