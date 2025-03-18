## `openjdk:25-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:0482ccbe64797e5694eadfc0a6b3111d6476b48a4485296b100c2c6d6e329813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-ea-jdk-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:bce729c42cccc08b156e61740ae68e0d9a923cfe715a50229bd6b847a65e1869
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318882861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195d580572429bd54dd50b1a521fe345c8ca1ff139c4243b7dbb561f811a2fb4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 17 Mar 2025 22:24:25 GMT
SHELL [cmd /s /c]
# Mon, 17 Mar 2025 22:24:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 17 Mar 2025 22:24:27 GMT
USER ContainerAdministrator
# Mon, 17 Mar 2025 22:24:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 17 Mar 2025 22:24:29 GMT
USER ContainerUser
# Mon, 17 Mar 2025 22:24:30 GMT
ENV JAVA_VERSION=25-ea+14
# Mon, 17 Mar 2025 22:24:38 GMT
COPY dir:3bbdecdaf44fd794a45fa39cf7b31efe4cc2d91c5e3e7c4c5333407317959149 in C:\openjdk-25 
# Mon, 17 Mar 2025 22:24:42 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 17 Mar 2025 22:24:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d092fe629d718380947d24acac5383c7cf7ff4acf0ff66bad60144f1b50b5f`  
		Last Modified: Mon, 17 Mar 2025 22:24:50 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398195166db260660e3c046850c8220bf8b0cc9ad5651f3c0f1a26e87cc464b8`  
		Last Modified: Mon, 17 Mar 2025 22:24:49 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d4815f02e9dd52421d238b3b0238e78d462229d3ba722a6bff3a36d622c520`  
		Last Modified: Mon, 17 Mar 2025 22:24:49 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e535147cd0916d53a51400fa36e43b0704112704bcd958fab9caf73735f3a2e`  
		Last Modified: Mon, 17 Mar 2025 22:24:49 GMT  
		Size: 68.7 KB (68666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d35055e45c1c777718d278258806e7c7dd442880920995cb61e404fc27d6b0`  
		Last Modified: Mon, 17 Mar 2025 22:24:48 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fca2129a31eed04da43d86f3b211d4ae862409b425ec16155b874219ff91e1`  
		Last Modified: Mon, 17 Mar 2025 22:24:47 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ae266edb8e048d818618639a49be880a0875c5d3da1bb14ffa566d57fd62da`  
		Last Modified: Mon, 17 Mar 2025 22:25:00 GMT  
		Size: 207.5 MB (207469646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833d018d62c4854a8fb40641363de6df9248b49e7070bad1136e8913ecf62fe6`  
		Last Modified: Mon, 17 Mar 2025 22:24:48 GMT  
		Size: 4.4 MB (4430628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6e137b9515d90e6b98b1760548a809b67690d1db02ffd11a5fb50614e23897`  
		Last Modified: Mon, 17 Mar 2025 22:24:47 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
