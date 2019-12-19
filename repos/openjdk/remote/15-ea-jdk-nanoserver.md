## `openjdk:15-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:fb084070af93639bed0618eb3ab6c74395dfe9861cefd74010d6b64afae6d00e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:15-ea-jdk-nanoserver` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:48cd89cb2d52f0bc04ee0ad7f433b85930fddc18b5f3209acf996afcea61aba9
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298267668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348add78702e97c82ce896ec0459defcb7c0e4d2dedd761a0b075d940e833df9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:49:48 GMT
SHELL [cmd /s /c]
# Thu, 19 Dec 2019 01:29:02 GMT
ENV JAVA_HOME=C:\openjdk-15
# Thu, 19 Dec 2019 01:29:03 GMT
USER ContainerAdministrator
# Thu, 19 Dec 2019 01:29:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Thu, 19 Dec 2019 01:29:16 GMT
USER ContainerUser
# Thu, 19 Dec 2019 01:29:18 GMT
ENV JAVA_VERSION=15-ea+1
# Thu, 19 Dec 2019 01:30:18 GMT
COPY dir:615f35b89aedbd1dd61875bf69bf0b61d00c73dd04e8c51ecd5f899cf740a76c in C:\openjdk-15 
# Thu, 19 Dec 2019 01:30:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 19 Dec 2019 01:30:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:163d55b77f49371136083ba8066ddbec4afad6e1f4fbba77fa4ffebc99a8098a`  
		Last Modified: Wed, 11 Dec 2019 20:01:21 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63bb05b94288d5ea0447e7c6b75a854704f420c56d3b13acab4d9b2e03cc3f4`  
		Last Modified: Thu, 19 Dec 2019 01:38:08 GMT  
		Size: 914.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64927380268ba75b4d8445c6eebea564ad1af3f6ffcd0ab9856b348138b44532`  
		Last Modified: Thu, 19 Dec 2019 01:38:08 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca8bce76a22921ecaa2f6065834a3d494b61f569022c5b64bf0c9fa9c5bc63c`  
		Last Modified: Thu, 19 Dec 2019 01:38:08 GMT  
		Size: 71.4 KB (71377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b95fb661adc21f04050381ea3e21b42927fa5df24d3b78a394b6e71e7992c12`  
		Last Modified: Thu, 19 Dec 2019 01:38:05 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fac2a6c7cfbff3964311aa7a8d95cbb2998f9cafd1bd6229032ca5e316355d`  
		Last Modified: Thu, 19 Dec 2019 01:38:05 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcfa8aca46069afc887dc0d1200168c5b3d4c6e9dd31b11f6834a1557a4fcb3`  
		Last Modified: Thu, 19 Dec 2019 01:38:27 GMT  
		Size: 193.6 MB (193647755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff9c34843682deba3e3449f1f3554571df66c8a291f0bdf0dd40787113be577`  
		Last Modified: Thu, 19 Dec 2019 01:38:06 GMT  
		Size: 3.4 MB (3436818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5813f9ba0ca7cfd52bd0e11663beb6ff4f083f58729dd82799a31f439153437`  
		Last Modified: Thu, 19 Dec 2019 01:38:05 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
