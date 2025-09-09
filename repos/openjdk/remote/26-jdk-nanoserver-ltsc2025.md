## `openjdk:26-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:9a645cdcb8c0936c63afe2cb81f8029f8a78a9446b381796e08613aa354ef614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `openjdk:26-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:0dc41e428b7c3aafdfed96afe156e2d75d12dbc39748225ec725e2d6aa0fe532
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.5 MB (412453210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec72e326ffb81a412f69605c8c7cfced95cb76bdf2e4935cdd35b9ee2e4ca93c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Mon, 08 Sep 2025 22:03:38 GMT
SHELL [cmd /s /c]
# Mon, 08 Sep 2025 22:03:39 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 08 Sep 2025 22:03:40 GMT
USER ContainerAdministrator
# Mon, 08 Sep 2025 22:03:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 08 Sep 2025 22:03:44 GMT
USER ContainerUser
# Mon, 08 Sep 2025 22:03:45 GMT
ENV JAVA_VERSION=26-ea+14
# Mon, 08 Sep 2025 22:03:54 GMT
COPY dir:7a6e05bab7ed4afc8034861a8ee41b1162c1c080c85bb9015a3a17ef93690785 in C:\openjdk-26 
# Mon, 08 Sep 2025 22:04:01 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 08 Sep 2025 22:04:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a2a5f2e0a531d0494aabdabee4653bd099c0c98d3b6376b79ce783d21e119d`  
		Last Modified: Mon, 08 Sep 2025 22:16:30 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1cb1478965bd8cc356a76a181d3d8cc873975ba4f9f8b43d4ba88351c85d4f`  
		Last Modified: Mon, 08 Sep 2025 22:16:33 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5dcfdf1b742d523e51b06e1913f275ae5a3b82edaa3a737aa0f41dd24face30`  
		Last Modified: Mon, 08 Sep 2025 22:16:37 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f56e83c0ac511793c6599c84480156bfa4b46a5f1c7ec5c063a92df38a8402c`  
		Last Modified: Mon, 08 Sep 2025 22:16:40 GMT  
		Size: 75.8 KB (75819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c949b9ae498a6a1ac92debb5201572a6d688f70f6d01745449f71a27d116f6`  
		Last Modified: Mon, 08 Sep 2025 22:16:45 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004b6e7105cd02831cb88a57e39ee1941578f467c49b229f8047ec4922ca1607`  
		Last Modified: Mon, 08 Sep 2025 22:16:47 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3e95a829d6baf7e5a73bb212c0a9c34bc34e523802a447f413952458aca34f`  
		Last Modified: Tue, 09 Sep 2025 00:25:26 GMT  
		Size: 218.8 MB (218787269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38b7a9589cbb11735f7d573cd34cb011042388ffb3a7e1eadb255b294597bd0`  
		Last Modified: Mon, 08 Sep 2025 22:16:51 GMT  
		Size: 114.4 KB (114423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e5cd4688bb9b32d06318d66c5d02e7fa242e4b29dce45a815d63af6a44fa96`  
		Last Modified: Mon, 08 Sep 2025 22:16:56 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
