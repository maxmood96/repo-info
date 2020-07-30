## `openjdk:8-nanoserver`

```console
$ docker pull openjdk@sha256:3933b48dec07fb42d919a57b64711bc2e5ec46e02a8389e2e497ba8d861341c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:8-nanoserver` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:c660ead4f0dddc1315094c4f78a6930406f5e581bedd9e0c29e0c77ff71a7aba
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 MB (201123671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c634f2c74532a6d716133d6e039cd2a26794815d4bc07bd99ea7cdf587a412db`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Jul 2020 13:50:07 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jul 2020 01:54:43 GMT
SHELL [cmd /s /c]
# Wed, 15 Jul 2020 02:34:08 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jul 2020 02:34:09 GMT
USER ContainerAdministrator
# Wed, 29 Jul 2020 01:38:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 29 Jul 2020 01:38:32 GMT
USER ContainerUser
# Thu, 30 Jul 2020 22:19:51 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:20:19 GMT
COPY dir:3c2880b061bc00940ee162754a64e55567e0dbb10e65b749277b54fa005ce8de in C:\openjdk-8 
# Thu, 30 Jul 2020 22:20:42 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:dc95608099543221ef539391bfece5c1ce37b97af9da457f5990349cab028a12`  
		Size: 100.9 MB (100895619 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f6486e4debac36806ed3527d9b1baea75c1a807e26baccdd0a2f521c814273f`  
		Last Modified: Wed, 15 Jul 2020 02:43:55 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635f616413e2ffeb2b698529474f16b802473016d0380fd29b21f12527e7006d`  
		Last Modified: Wed, 15 Jul 2020 02:54:29 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a9bf2169040f2fa44109296c3dc79cd3e81ec224a0a19ae4d74f3866e4bac3`  
		Last Modified: Wed, 15 Jul 2020 02:54:29 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12919e4a3f7690ed0c169e50a54145f9ad295248806072f541b2753c617e25c7`  
		Last Modified: Wed, 29 Jul 2020 01:55:54 GMT  
		Size: 66.4 KB (66363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a3ba49404160f0c5b7fe7e56cc630dc53340e9e3ce7327144589c193f51427`  
		Last Modified: Wed, 29 Jul 2020 01:55:53 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c8250f9dab00bfef751c16f2eed1d51cbfcc3be032a34e9cd464b0c26eaa39`  
		Last Modified: Thu, 30 Jul 2020 22:28:15 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfadd4be7c871e1d5d0559b191bc7658d9556ea625d35c3b25877e38c466bd9c`  
		Last Modified: Thu, 30 Jul 2020 22:28:27 GMT  
		Size: 100.1 MB (100110877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0761adeaab8116029e865690f2d5e5e010af6a2cb5d6e032375945f3a01d2fc2`  
		Last Modified: Thu, 30 Jul 2020 22:28:16 GMT  
		Size: 46.4 KB (46388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
