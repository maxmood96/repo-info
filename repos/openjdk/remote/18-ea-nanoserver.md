## `openjdk:18-ea-nanoserver`

```console
$ docker pull openjdk@sha256:4cc57c56429c405eeb9ef705545284c32ff1f22a0059d6c06a48819cd86c19e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `openjdk:18-ea-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull openjdk@sha256:32659c87be060df924469a68936c29e3e27ccaa472adaff4768e80f336cf30e0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289344726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f66bf7eb8eab177155611c984642cc27ccaffa4928e5b9ba729a86d18c6263`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 00:38:23 GMT
SHELL [cmd /s /c]
# Wed, 15 Sep 2021 00:38:24 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 15 Sep 2021 00:38:25 GMT
USER ContainerAdministrator
# Wed, 15 Sep 2021 00:38:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 Sep 2021 00:38:37 GMT
USER ContainerUser
# Sat, 09 Oct 2021 00:19:05 GMT
ENV JAVA_VERSION=18-ea+18
# Sat, 09 Oct 2021 00:19:21 GMT
COPY dir:dcda33f24f8dfe8fd8921e2cc6263e8b226b9f16c44f04a813f88734e09a209f in C:\openjdk-18 
# Sat, 09 Oct 2021 00:19:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 09 Oct 2021 00:19:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:807d06303c39b2317729754a4c7ad6501e59c16ee464f8f671f9947774f62f72`  
		Last Modified: Wed, 15 Sep 2021 01:10:56 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353abb4dcfd1456117623d23e4be07d7d5c9e18c7ddea8dfb6225f99efa904b9`  
		Last Modified: Wed, 15 Sep 2021 01:10:55 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6beb0bff60eb1dfb88e1010454b9aaf8f176f0d004a94fefdedb88d8e7e2a4`  
		Last Modified: Wed, 15 Sep 2021 01:10:55 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bcb79c10ca3fae0a02ab85be6ab15af3a4ac4d7a0b8b54fd7a9c12cdd0b203`  
		Last Modified: Wed, 15 Sep 2021 01:10:55 GMT  
		Size: 75.1 KB (75126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57b1aff54bbfc95746d48fc4f9d9afbb2f1f02e7d7006d7a7d6265ae52f9289`  
		Last Modified: Wed, 15 Sep 2021 01:10:52 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c7592a35fe2146629854fa02cda2b7ce87e70f500fad3a8da98c0447d16d45`  
		Last Modified: Sat, 09 Oct 2021 00:25:33 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3fdb41723adc707ce5066658092e9881c4dadbfeb66794f711ae79d0ed425a`  
		Last Modified: Sat, 09 Oct 2021 00:25:53 GMT  
		Size: 183.0 MB (183034019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d608b36e626a9cf675a567f6658e9b688bbb1fac3cf64b3e4fb92dd762a7bf`  
		Last Modified: Sat, 09 Oct 2021 00:25:34 GMT  
		Size: 3.5 MB (3525222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036edd9f73f2f96d6eb5ba5ba87dea2092186b0d311ee599c10f7805db345222`  
		Last Modified: Sat, 09 Oct 2021 00:25:33 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
