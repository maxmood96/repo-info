## `openjdk:8-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:34b51edae137cfd983590a213ece998f67024df1be85cda23d8d65f9b6bdb60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `openjdk:8-jre-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull openjdk@sha256:edd84f31ef90c482f645b4f45cc71ee373d04c3e3f512ed13854335cd1fd61c0
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139574535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc8f79c831011c0f73d5b5c0c8059b32ff07f494a6c2926f9ec6c9e9e1bd374`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 18:58:23 GMT
SHELL [cmd /s /c]
# Wed, 09 Dec 2020 19:24:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Dec 2020 19:24:15 GMT
USER ContainerAdministrator
# Wed, 09 Dec 2020 19:24:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 09 Dec 2020 19:24:27 GMT
USER ContainerUser
# Wed, 09 Dec 2020 19:24:27 GMT
ENV JAVA_VERSION=8u275
# Wed, 09 Dec 2020 19:28:20 GMT
COPY dir:9c574feda3d434860f596ed9945da2b2916773d80cfb9282fa700c98a8998c43 in C:\openjdk-8 
# Wed, 09 Dec 2020 19:28:36 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fe9a51a0164bd1c063cbda08c4e22dc4f5d04a8047a3951d7441f37fb93c57f2`  
		Last Modified: Wed, 09 Dec 2020 19:34:04 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad29805a2e79817ec885e95d10ac3666c7db47089b0e4aee98814630ab80f963`  
		Last Modified: Wed, 09 Dec 2020 19:48:37 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a45950b9ccb0b9ab48b1d0f5d562bbd06a4bee9d1ec5353f3b5cb345cdc333`  
		Last Modified: Wed, 09 Dec 2020 19:48:37 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2512814db550f049e4de762fa28d22a7733422d787875d1df655c3f1b78f95b`  
		Last Modified: Wed, 09 Dec 2020 19:48:34 GMT  
		Size: 67.7 KB (67702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd51424d982ea438cb6960b394da897cbdaaf677cc73eca37ed49d8f4350c06`  
		Last Modified: Wed, 09 Dec 2020 19:48:34 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f8cfd6713432c52822dc67dbff8dbba5fac05f979f0b2cc11758183ddbe4b2`  
		Last Modified: Wed, 09 Dec 2020 19:48:34 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51127394d4023765fa0ae0d67be224a1daff0848f9451c620bff3a155d25abfb`  
		Last Modified: Wed, 09 Dec 2020 19:49:58 GMT  
		Size: 38.2 MB (38190990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b616466a3b3071abe0cb80540f76ce03910d3fbbf6bf91353b7c414e297054d6`  
		Last Modified: Wed, 09 Dec 2020 19:49:52 GMT  
		Size: 46.7 KB (46683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
