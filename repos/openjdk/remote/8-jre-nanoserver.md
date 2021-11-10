## `openjdk:8-jre-nanoserver`

```console
$ docker pull openjdk@sha256:b6e23e12bf617a5038b014b5e16d00e421b181c0507125ecd42308b861539872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `openjdk:8-jre-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull openjdk@sha256:f689b381e077e5f78d315e206d53fbdae683505f54ac540b83bef4ee73c86d01
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141171045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cf510fe11b5911462752cee8ea8700cb7270ce00300bf21039f7a54a947d16`
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
# Wed, 10 Nov 2021 21:00:22 GMT
COPY dir:d01eca1f47b40119ea7401e87f8309ebbb3c59555f496ebfb4562b12d58cd948 in C:\openjdk-8 
# Wed, 10 Nov 2021 21:00:32 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
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
	-	`sha256:03aa365e7b0202ec941ac5d59f8126e34e7aa799037062ece175032af9b768d0`  
		Last Modified: Wed, 10 Nov 2021 21:35:21 GMT  
		Size: 38.2 MB (38229969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcdb70613d6d7939050af33ca7cd703e71f24c8f9ff04d9e977f27c1fada56d`  
		Last Modified: Wed, 10 Nov 2021 21:35:16 GMT  
		Size: 82.4 KB (82382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
