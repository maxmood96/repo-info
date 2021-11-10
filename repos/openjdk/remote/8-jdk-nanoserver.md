## `openjdk:8-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:5594ddb58b45c6bf58e4290d7a940195a073c9bd069ab51bcf51b763611be25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `openjdk:8-jdk-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull openjdk@sha256:20b7a3353147f63e07330dd4753a7a0d924c8c02561a393a71101929177691bb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204014696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be0350b0dd482eb0e56f6b18c69fb30ae51ee5b23fdfb3eeca84f2aac1aa597`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:13:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Nov 2021 20:56:30 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Nov 2021 20:56:31 GMT
USER ContainerAdministrator
# Wed, 10 Nov 2021 20:56:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Nov 2021 20:56:40 GMT
USER ContainerUser
# Wed, 10 Nov 2021 20:56:40 GMT
ENV JAVA_VERSION=8u312
# Wed, 10 Nov 2021 20:56:55 GMT
COPY dir:3a5581b2700e30ac96b7aaa667bdc25cdca1d6451f9f3d58913682ddf8d74e71 in C:\openjdk-8 
# Wed, 10 Nov 2021 20:57:06 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e60ec86b90e1492e0e0ed2cbebcf624990a34862e24207343fd85b84b3544c8e`  
		Last Modified: Wed, 10 Nov 2021 18:01:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aa251b7d3a5a75e1710a49ac7756cc1140f28ba0a05b1a67217ceafb4848d5`  
		Last Modified: Wed, 10 Nov 2021 21:34:06 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f30bfd5ed5f164a11037221dc17e6e10c482c1d510f3c3770da7c2fcafc9e13`  
		Last Modified: Wed, 10 Nov 2021 21:34:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf2edd8c7b4081ec9b6a291221f2f5a18351d25f07f5e1818dc705cf84867cf`  
		Last Modified: Wed, 10 Nov 2021 21:34:04 GMT  
		Size: 69.9 KB (69932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f4f49aef9529111750fdab992102db5bd3284becf179741643545e0b04b19c`  
		Last Modified: Wed, 10 Nov 2021 21:34:04 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4646e1fc59af14a84d2c9b550cd1616d7bce4bd8c9562c1f4b10f343b28bb485`  
		Last Modified: Wed, 10 Nov 2021 21:34:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ae9681e747673162575826934522b3dca780a560b87ae17d30e050d47ed077`  
		Last Modified: Wed, 10 Nov 2021 21:34:15 GMT  
		Size: 101.1 MB (101073226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffe4f15f1160909cbd973eea0a25fe10540b59d9756c40834cd06058915b995`  
		Last Modified: Wed, 10 Nov 2021 21:34:04 GMT  
		Size: 82.8 KB (82776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
