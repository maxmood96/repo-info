## `openjdk:26-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:418a20d55bd499a86c77b74f1da5ba17d71f59176a36216c648c91e86754e5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:26-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:2c2e38295c43b714c87c6964e4c28cce7387df80f4425e1f3c28f01650a0f44c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.2 MB (424240673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7164b37697822053fd08765e173d5e58c63798e29f7b77ae3eb1682485b125`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 21:12:53 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:17:04 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 09 Dec 2025 21:17:05 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:17:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 09 Dec 2025 21:17:06 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:17:06 GMT
ENV JAVA_VERSION=26-ea+27
# Tue, 09 Dec 2025 21:17:27 GMT
COPY dir:babad47417a0162dfe31675fb569b90c77d833ec4f406c1de246f79f46496cd3 in C:\openjdk-26 
# Tue, 09 Dec 2025 21:17:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 09 Dec 2025 21:17:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3aa2fd9c43d5870304ea449c22f4fbf73f16c064a13e04297c92a2a200461b`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbf61aa720fb8a66cda18f247270d82d9d1900f30fc68a65de202e584757ad7`  
		Last Modified: Tue, 09 Dec 2025 21:17:58 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f4ac1961aaee9c789a2877b20e939a5d484c55e636a0ae5768311990da06c1`  
		Last Modified: Tue, 09 Dec 2025 21:17:58 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af51aed34907716c8ecf71484166483e309e46bfc4f54dbeb12c25ebea28a66`  
		Last Modified: Tue, 09 Dec 2025 21:17:58 GMT  
		Size: 72.0 KB (71993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b5d3a323ea1dd8ae95e9c73585613dcd1880fcb19857e492e4098178a826aa`  
		Last Modified: Tue, 09 Dec 2025 21:17:58 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139cf1122bc374ccbeaed1f2bdf63c5ed8f4c3a16197ba9860bb3b002a02cb63`  
		Last Modified: Tue, 09 Dec 2025 21:17:58 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52918a8aaab9dd50dec1075db72f1f767116977c9f11865f6428ec74144c770f`  
		Last Modified: Tue, 09 Dec 2025 21:18:11 GMT  
		Size: 225.2 MB (225175476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ec277194870beca5d9a99467def64da8bd5e3ece3bf3a5cb8d2d5a65b5a48c`  
		Last Modified: Tue, 09 Dec 2025 21:17:59 GMT  
		Size: 112.8 KB (112808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d32385a60ea679717ca5e43f15a30984e50e447ab8a08d1b9a4c6fb979d15e`  
		Last Modified: Tue, 09 Dec 2025 21:17:58 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
