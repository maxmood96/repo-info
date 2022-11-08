## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:4b5143f5f5371f189743839561dbead020be2a5e23fff5bb99bf229bcbcbc379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1249; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:3d0b8c4a5395e2dc9384264d0393bb5479e7dffdfae6eb5a4f92679046580295
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314772628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecb14384faa6abd8812ac7b946da0fec99a1f8b4d071abb87dfd2bb5c4dd212`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 07:21:30 GMT
RUN Apply image 10.0.20348.1249
# Tue, 08 Nov 2022 19:27:23 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 19:29:25 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 08 Nov 2022 19:29:26 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 08 Nov 2022 19:29:27 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 19:29:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 19:29:40 GMT
USER ContainerUser
# Tue, 08 Nov 2022 19:29:58 GMT
COPY dir:cba9eceeddb80383417f5e5518328c343fc4183981a343fca253ea7c2e4dfda5 in C:\openjdk-11 
# Tue, 08 Nov 2022 19:30:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Nov 2022 19:30:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72e5d750fe8c1a32d4a26ef3b4a4e1f6124ac079b142f12724af2abfcba1c8b3`  
		Last Modified: Tue, 08 Nov 2022 19:57:58 GMT  
		Size: 122.1 MB (122092167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd83067a7e6c6d9dab3ac0265a21919de95a0bf4e737e647fbf3e43c9874b0`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf64ef5841c3055c97da30afe94e91f36d8258ef461b52540da9903c4e3bc9a`  
		Last Modified: Tue, 08 Nov 2022 19:58:33 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c375a4f91fe23421131785b0b42e01c977a392cf2b3e31402bf0d22f9485b2`  
		Last Modified: Tue, 08 Nov 2022 19:58:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37f60d8c806f3324c10a3f609dd590835d2f256a88a14d5555cbee6050df6e4`  
		Last Modified: Tue, 08 Nov 2022 19:58:32 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea17a3ec8151119077e9676e7507f58607330aade351454cc2b611ce183fdc90`  
		Last Modified: Tue, 08 Nov 2022 19:58:30 GMT  
		Size: 85.1 KB (85094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d30911c1c2bad5db46115e443e5a3fb3242f0d01dae68a8b470990aee8b83c`  
		Last Modified: Tue, 08 Nov 2022 19:58:30 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99d50bef7a099fe6463304b115c4b24172dac9bec424c286ad03ec798cd562b`  
		Last Modified: Tue, 08 Nov 2022 19:58:51 GMT  
		Size: 192.5 MB (192525543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785564f2b554d5b86b2eaeaea535fcc4d4f041c73321ad3988209f5a1ef2ff60`  
		Last Modified: Tue, 08 Nov 2022 19:58:30 GMT  
		Size: 63.0 KB (63035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274fb86a4f00c053ca29c6dd7db990ee5829915e5bd225df86168f7fe269fea7`  
		Last Modified: Tue, 08 Nov 2022 19:58:30 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
