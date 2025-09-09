## `openjdk:26-ea-14-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:2eab13a4ab8531c6dfa347c017ecfadf186adfd60c586ec7c7a06303df2de2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-ea-14-jdk-nanoserver` - windows version 10.0.26100.4946; amd64

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

### `openjdk:26-ea-14-jdk-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:e93c6f1737e57bc02f5187f5683afeab0ad0d3f54f41db45ddac62a4c5ef3871
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341624469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df848f156c96b9e8957322f9319e2de14ed0080f2f5f81dfa6b0d419d1296e9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Mon, 08 Sep 2025 21:34:44 GMT
SHELL [cmd /s /c]
# Mon, 08 Sep 2025 21:34:45 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 08 Sep 2025 21:34:46 GMT
USER ContainerAdministrator
# Mon, 08 Sep 2025 21:35:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 08 Sep 2025 21:35:13 GMT
USER ContainerUser
# Mon, 08 Sep 2025 21:35:14 GMT
ENV JAVA_VERSION=26-ea+14
# Mon, 08 Sep 2025 21:35:25 GMT
COPY dir:7a6e05bab7ed4afc8034861a8ee41b1162c1c080c85bb9015a3a17ef93690785 in C:\openjdk-26 
# Mon, 08 Sep 2025 21:35:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 08 Sep 2025 21:35:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bd8ad8f916313beaba04a8333b9acf8d68d0e33738e28f8559aaafd490bb5a`  
		Last Modified: Mon, 08 Sep 2025 22:26:27 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8424b3fe804d52e6961f00964a6245c883b91e1a17f6620620988e08d064631`  
		Last Modified: Mon, 08 Sep 2025 22:26:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8bc7b9e5f7d887b3b3ac4f49c574b2904106a50936367cce59459dcbe16ebf`  
		Last Modified: Mon, 08 Sep 2025 22:26:27 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059593f1d9faabe3044cc8d11123d4ec526c3a91d03dbab0c6aabf7a57f1ea35`  
		Last Modified: Mon, 08 Sep 2025 22:26:27 GMT  
		Size: 77.8 KB (77775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fb4afff22bd1c9edb53f294279db8d7a2ce0c00a7e36b206365745d3f58475`  
		Last Modified: Mon, 08 Sep 2025 22:26:27 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59ba3cadd7d0f29fc5a3147c384415abbcb266c0b52c98d0b73055928edb91c`  
		Last Modified: Mon, 08 Sep 2025 22:26:27 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1c47a3128aa629e7b0c2d97b391a76accd29effa2b0d386757476647746e36`  
		Last Modified: Tue, 09 Sep 2025 00:26:25 GMT  
		Size: 218.8 MB (218784919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc16c79a9067b26eac658235d50e7caee7d47fe2da4082906d99a3a4591eadc`  
		Last Modified: Mon, 08 Sep 2025 22:26:28 GMT  
		Size: 95.2 KB (95213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a92117fbfa883016829e7b44e35b8117fc11b7312542b027aeebba0b3b2a938`  
		Last Modified: Mon, 08 Sep 2025 22:26:27 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
