## `openjdk:26-ea-24-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:de18e2b6adb38466ca1f5982c1988c88671e011545d3d3c02375d613757a9c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `openjdk:26-ea-24-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:7b7884243ed023d085dec398ff39a730aee244346286846e36b2ac19fee8e2cd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.3 MB (421250970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fd17ccaf7cebf8c2264edd01c4f810b4b2c81cbff5a85c1399e1bf74a39bf3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 18 Nov 2025 00:45:33 GMT
SHELL [cmd /s /c]
# Tue, 18 Nov 2025 00:45:34 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 18 Nov 2025 00:45:35 GMT
USER ContainerAdministrator
# Tue, 18 Nov 2025 00:45:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 18 Nov 2025 00:45:43 GMT
USER ContainerUser
# Tue, 18 Nov 2025 00:45:44 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 00:46:27 GMT
COPY dir:580fa45a384b12cb70c75bbdb47b5399a06812987f2bb40365d6f1c31468fec4 in C:\openjdk-26 
# Tue, 18 Nov 2025 00:46:33 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 18 Nov 2025 00:46:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdc9adaebb0e2db8d513eb5331987e9eab8584be574b803f294162fb9a706ea`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6462b50fe72ed7962477a69d48cb04a029e244cd6cb5852acd5072b03ed85b5`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020a7d27b5fedf5ae34e14337f8cc220e51f8acfc0eb50f5dcfe0bdf04daf099`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b67d8e48a00015c8297185a4d0a75eb5509a9c758ee6c87c23addab45aec27`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 70.4 KB (70404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1de02e08bd00e70d065e2e39a3867b1954fa45d0b6061438e82e9b18bfd72c`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c9d2463df6058b30ece2d49d4e9817ec4dda47d1c649fa6c1a0f37940083e2`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732d14b69a38e3b2ca234b9a3df5c4d3d405ea770b2d2a06027d58660c8c8c7`  
		Last Modified: Tue, 18 Nov 2025 01:23:58 GMT  
		Size: 223.2 MB (223154105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6aaab9f372542f76a5d86bc391ceb39e562f7db9fdd76beda360eb37a1ab5dc`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 83.5 KB (83549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88c6e598900e3770b59fd7e2c055ac7a548e531c7fc36b4cead9c43add8177f`  
		Last Modified: Tue, 18 Nov 2025 00:47:52 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
