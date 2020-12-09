## `openjdk:8u275-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:62a662d71dce0d3f2bda4458cf54d9439d79c148d13095cd5db8d0fc964bc96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `openjdk:8u275-jdk-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull openjdk@sha256:60b4bcf1c2af327aa51440fadb2c88f0f61e662ff64d05e7022af0e2c46bddc7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202364853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3102ee440d4be331cebcf6df98ffc76eee1822b06d2c450b56911b389f52b2e3`
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
# Wed, 09 Dec 2020 19:24:55 GMT
COPY dir:0892804dd065b22adc43ce2caaaf5966043723850b9894e42783006f86478881 in C:\openjdk-8 
# Wed, 09 Dec 2020 19:25:14 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version
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
	-	`sha256:cfb7f166cd890350aaecfe7a8c66186e51b8ac54ef5237acec44b0a8f449feb4`  
		Last Modified: Wed, 09 Dec 2020 19:48:46 GMT  
		Size: 101.0 MB (100973007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a7fea0cadd3dee90feea5175f7df28c0b7f089cf24a2839b052146bf752afc`  
		Last Modified: Wed, 09 Dec 2020 19:48:34 GMT  
		Size: 55.0 KB (54984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
