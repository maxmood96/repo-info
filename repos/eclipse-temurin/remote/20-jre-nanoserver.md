## `eclipse-temurin:20-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a157f26b419889acaefadcf73ac7bd07c16e4dbc550825ca63bb46993611dcf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1970; amd64
	-	windows version 10.0.17763.4851; amd64

### `eclipse-temurin:20-jre-nanoserver` - windows version 10.0.20348.1970; amd64

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

### `eclipse-temurin:20-jre-nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull eclipse-temurin@sha256:fe92ba10ce2db30bee9a41e7403aa20526eda98105017139733281f59d74634a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153549942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983ac3091e237ab06268c8a510b7523dfddbe5f10381d23a3729f1b2e80236d9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 02:29:44 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 03:11:56 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 13 Sep 2023 03:11:57 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 13 Sep 2023 03:11:58 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 03:12:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 03:12:10 GMT
USER ContainerUser
# Wed, 13 Sep 2023 03:18:26 GMT
COPY dir:7e69bb3960973ab39fc2ba0552343e70b32506a25a841e69600e9c49be1d11aa in C:\openjdk-20 
# Wed, 13 Sep 2023 03:28:48 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5bcbc9b0f0398bf8f14c235b24ba85d9acacf855518119cd1ce338a235a15`  
		Last Modified: Wed, 13 Sep 2023 03:36:33 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e8f8b6a865f909378039e86ae667b406118a25b3a153bfc989219634e11931`  
		Last Modified: Wed, 13 Sep 2023 03:45:27 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a9140c6a0cfd95053c573337fe186e7c914e2cddc4ded5396d633f8168d811`  
		Last Modified: Wed, 13 Sep 2023 03:45:27 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ad06a8f04950c85d8c4f1f0bf2976f8279ad5bddaa2eeb25ac627a5322ee4f`  
		Last Modified: Wed, 13 Sep 2023 03:45:27 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d27824264e82d62f11110ce00b426e3404ff58b09ac8981602874b9d0f4518a`  
		Last Modified: Wed, 13 Sep 2023 03:45:25 GMT  
		Size: 68.8 KB (68806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03cb3c15586ae832292360f56f1ac78eaf96af2d83bcb41622737199018f5d2`  
		Last Modified: Wed, 13 Sep 2023 03:45:25 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658d250f1e13f7f305f2b10bb024d9f491b8a54238a4913ada91247e962d180e`  
		Last Modified: Wed, 13 Sep 2023 03:46:52 GMT  
		Size: 45.8 MB (45836457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879ce7ffdf7dcf733f52083c70fb6374f9fb13dddb7bf6c7394fb51af297ab8e`  
		Last Modified: Wed, 13 Sep 2023 03:46:43 GMT  
		Size: 3.1 MB (3146455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
