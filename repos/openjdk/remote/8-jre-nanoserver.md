## `openjdk:8-jre-nanoserver`

```console
$ docker pull openjdk@sha256:a2091c02adcb6297faf53f668e162d99efc517cc06ad9eaf2b6c1b0f00f99e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:8-jre-nanoserver` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:008eb2db66306e0a73940595b9856ff691ffb71a0c667bee9f477dcac5449cbf
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138438547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f85901ab74cc3f342bd34696516510dab322c2de405e4b06abfc6e71bf8a22`
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
# Wed, 29 Jul 2020 01:38:33 GMT
ENV JAVA_VERSION=8u262
# Wed, 29 Jul 2020 01:42:28 GMT
COPY dir:9eeb064c358340bf4c43c46608fc234381de425bcb675b8260eb038f2fb7541d in C:\openjdk-8 
# Wed, 29 Jul 2020 01:42:45 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version
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
	-	`sha256:8d958a1c92873cb903a6771ee4c7b07969f3585c9163f927bb001aa92a6bc7c6`  
		Last Modified: Wed, 29 Jul 2020 01:55:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ce0adc7ecb8b89b3e1171d04c86853ebc6de96cad6db758e9c9ff5505695a3`  
		Last Modified: Wed, 29 Jul 2020 01:57:03 GMT  
		Size: 37.4 MB (37426658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d91630ea23f19892a19e819766fda3abe91e0d81eba75ae157cff184ed312d`  
		Last Modified: Wed, 29 Jul 2020 01:56:57 GMT  
		Size: 45.5 KB (45462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
