## `openjdk:14-ea-nanoserver`

```console
$ docker pull openjdk@sha256:928d2009372408a69c072e307e63d7ae79f6ae2a256a6708d968b63ad1858df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:14-ea-nanoserver` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:1bd8d733e873bfe6999a773d7e6cbc8a88729ae80c8144efeae9f51bd9544420
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298461745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8d1fa11642dc66a184e1aa8271bd6ddfe2901b883253ead078601b24d7ad37`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:49:48 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2019 18:49:50 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 11 Dec 2019 18:49:51 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2019 18:50:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Dec 2019 18:50:07 GMT
USER ContainerUser
# Thu, 19 Dec 2019 23:38:00 GMT
ENV JAVA_VERSION=14-ea+28
# Thu, 19 Dec 2019 23:38:55 GMT
COPY dir:40ffa59b77af7c3aa7edfb5cafa727af50771b0fdb1554864d83f0b5a33221ab in C:\openjdk-14 
# Thu, 19 Dec 2019 23:39:16 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 19 Dec 2019 23:39:17 GMT
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
	-	`sha256:9326e4caa8f459874d77c281820948a0fa2e558568f484250684f714e368c0bc`  
		Last Modified: Wed, 11 Dec 2019 20:01:19 GMT  
		Size: 953.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07bbc07ec7d9f59279b56946327222e61b8d576bc34eb8b70be4aa88b484d87`  
		Last Modified: Wed, 11 Dec 2019 20:01:19 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c25567424a9bb0685aa9d0cc78a53b800a3447fff914466146890e6bf40dcdd`  
		Last Modified: Wed, 11 Dec 2019 20:01:19 GMT  
		Size: 63.9 KB (63920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6607ef629cd6ba3de9b2b3f57cdc6172ca483c4f285428321d4b04ce9b321db8`  
		Last Modified: Wed, 11 Dec 2019 20:01:16 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379a3fa4d96b0eb0564cfcc12feeb912260564458dab76c8f7c0b8c8940fc13f`  
		Last Modified: Thu, 19 Dec 2019 23:50:21 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e26ed3eb4cb87d8d83cdfdd444795b00f9116c995e3be9232602700e1944cf1`  
		Last Modified: Thu, 19 Dec 2019 23:51:00 GMT  
		Size: 193.8 MB (193793825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c484920a35b19bba1952934fa888096181aae2da4ebe792fb467961fc3782be`  
		Last Modified: Thu, 19 Dec 2019 23:50:23 GMT  
		Size: 3.5 MB (3492247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd59a0803176a5772e50abd307ae12f4c07b4fe85296fd323561394f09c8558`  
		Last Modified: Thu, 19 Dec 2019 23:50:21 GMT  
		Size: 925.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
