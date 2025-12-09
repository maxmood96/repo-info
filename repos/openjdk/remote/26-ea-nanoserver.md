## `openjdk:26-ea-nanoserver`

```console
$ docker pull openjdk@sha256:d23bbe1ddce8ef655e394c989773ea5e3e01db83cc7dc4240bfac5c4d8484fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `openjdk:26-ea-nanoserver` - windows version 10.0.26100.7462; amd64

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

### `openjdk:26-ea-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:03e3e96ad22a3b4b036b9e37b0f79820401b20314cc2c7c453a8be9cf9299892
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.7 MB (351724897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c051f232654b53061e30eb83fb35e7b6d2a5bf0c56cc9764a5442deb4c37f3c6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:49 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:16:08 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 09 Dec 2025 21:16:08 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:16:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 09 Dec 2025 21:16:10 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:16:11 GMT
ENV JAVA_VERSION=26-ea+27
# Tue, 09 Dec 2025 21:16:19 GMT
COPY dir:babad47417a0162dfe31675fb569b90c77d833ec4f406c1de246f79f46496cd3 in C:\openjdk-26 
# Tue, 09 Dec 2025 21:16:25 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 09 Dec 2025 21:16:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39379f4668f7979dc09bdc5a0a70c7fe2057bbe447911ca76de5488139977d7`  
		Last Modified: Tue, 09 Dec 2025 21:13:27 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a09159775d71e6775a1f779f343a43cdea2a1bfc39049fa2b0e93f145eea02d`  
		Last Modified: Tue, 09 Dec 2025 21:16:54 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ff223f5db7133c511d518ff0d369337579d35818cd341552520f30389c2ccf`  
		Last Modified: Tue, 09 Dec 2025 21:16:55 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a30f18dedbf874e32b28c75e8334d1a971ed77424ff7f3afd9cd5af9c99e72b`  
		Last Modified: Tue, 09 Dec 2025 21:16:54 GMT  
		Size: 77.3 KB (77279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013b6a61dea8dd142bf6c5c500d1f429780303dce44786ad0f698dbac187bb30`  
		Last Modified: Tue, 09 Dec 2025 21:16:54 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10f549c03b14a0b031e2b0a7d2bb329823990168da854fa6448bf16d1df79ae`  
		Last Modified: Tue, 09 Dec 2025 21:16:54 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7630155f7a210731091d1dbee20437f9c82d6c85856b3af43b6a3f74f726ec`  
		Last Modified: Tue, 09 Dec 2025 21:17:04 GMT  
		Size: 225.2 MB (225175683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3ccc94df4e6f900868b1ec513a85ed41e45da54accf67e2e18cd68a758c218`  
		Last Modified: Tue, 09 Dec 2025 21:16:54 GMT  
		Size: 107.3 KB (107292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a15de56d8491f00caa8bc069f42b34cd4068152a2caf09a4d234d0857dade9`  
		Last Modified: Tue, 09 Dec 2025 21:16:54 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
