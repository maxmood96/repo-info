## `eclipse-temurin:8u432-b06-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:40ec2db7dd98ae76c36454c592517a9818a9519d03b1e7200f17c557555b70f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `eclipse-temurin:8u432-b06-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2966; amd64

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
		Size: 78.3 KB (78275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8992290c525664c73ea30f1986873a9ae697a4146e2b88ae4f79119f60ae36`  
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
