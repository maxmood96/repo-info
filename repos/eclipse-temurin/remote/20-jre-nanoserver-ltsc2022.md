## `eclipse-temurin:20-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:6dacfdcd37376bfcc96831a925f599a259df5bb23cb38256a049ca6afa707acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `eclipse-temurin:20-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull eclipse-temurin@sha256:06ce6dce9838b80086de2a7d1897eeb4410e2da663dfcded03c20a3be687a776
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166572179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b52dcc14ec6343f47bb0653759139f49008b7d02a725578ef4906305c3e40a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Sep 2023 00:20:14 GMT
RUN Apply image 10.0.20348.1970
# Wed, 13 Sep 2023 03:28:54 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 03:32:14 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 13 Sep 2023 03:32:14 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 13 Sep 2023 03:32:15 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 03:32:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 03:32:22 GMT
USER ContainerUser
# Wed, 13 Sep 2023 03:33:06 GMT
COPY dir:7e69bb3960973ab39fc2ba0552343e70b32506a25a841e69600e9c49be1d11aa in C:\openjdk-20 
# Wed, 13 Sep 2023 03:33:14 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8f8cef0759210af9d01a2fb45d79956a2db738bbd3734b7244b17e14ad945cab`  
		Last Modified: Tue, 12 Sep 2023 18:47:39 GMT  
		Size: 120.6 MB (120567584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d67aef4c483590cefd40495efc212f13e4c62993e8036c20bb4e19bc8620508`  
		Last Modified: Wed, 13 Sep 2023 03:47:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4634269db964b0398e0eee8857f6f9e741e0d77d9756b734e52fcd50cb90b109`  
		Last Modified: Wed, 13 Sep 2023 03:49:26 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9523788cf112297aadea5c11363b6dd4dcb812dfcd605fd7e1ceaefa16a2ff6f`  
		Last Modified: Wed, 13 Sep 2023 03:49:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a66cd8fbc017b1506f1c2ee6beb4e7138aa38afbb0714e051472ea5231e300`  
		Last Modified: Wed, 13 Sep 2023 03:49:26 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca8dcce37e91e33e93bbe27a72bc9a9ccbafc84566f773a38beb132df9d2d9c`  
		Last Modified: Wed, 13 Sep 2023 03:49:24 GMT  
		Size: 84.7 KB (84679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7648837fcd42ac620828b08d39b107704a68af2bbb97daa5752870a62a719690`  
		Last Modified: Wed, 13 Sep 2023 03:49:24 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee23bb94bed9ce2659550156499d7b434554bcef48609e257ae3fd97ee02271`  
		Last Modified: Wed, 13 Sep 2023 03:50:08 GMT  
		Size: 45.9 MB (45852673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b69935fa640c3ddac6ddd5c453921dc41bc072b0a81462c1f06483309022b2f`  
		Last Modified: Wed, 13 Sep 2023 03:49:58 GMT  
		Size: 62.0 KB (62022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
