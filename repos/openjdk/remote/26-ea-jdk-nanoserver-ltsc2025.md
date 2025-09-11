## `openjdk:26-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:4a9784ca37c2c0ce4b40af29fa781df216fd98952e1b7a37a7bc1b486e79379d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `openjdk:26-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:e7362bbf530e576b048ee80d9209e687e56de4bb6b0a0f475c1b99a35036a488
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.5 MB (412536286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7196bd3f076c528fd96cf7c7887f012f8dced051293cb671c23cfa55e49e3596`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Wed, 10 Sep 2025 22:19:29 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:21:12 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 10 Sep 2025 22:21:13 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:21:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Sep 2025 22:21:14 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:21:15 GMT
ENV JAVA_VERSION=26-ea+14
# Wed, 10 Sep 2025 22:21:23 GMT
COPY dir:d50107523f417125c2242d5366bf04295424e0a959b88dfcf6f8074b4fb0cc43 in C:\openjdk-26 
# Wed, 10 Sep 2025 22:21:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Sep 2025 22:21:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b636e08ca81d9926ec06f59f2f2089b03b88ddb100925b01583e5bd9db293d3e`  
		Last Modified: Wed, 10 Sep 2025 22:39:50 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cac2c461109f28efe7c22f2dbe064ee634ee9c712a4d183706b8a8334327e9`  
		Last Modified: Wed, 10 Sep 2025 22:22:02 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc53814af96a510d785fbaf7c004fd861f8999b8ae62635ba4f4c795a0a15a52`  
		Last Modified: Wed, 10 Sep 2025 22:22:02 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26eeb136bb40f5a9f9bc6e5e7732c20350cdb26debc8a180105de11627396c2`  
		Last Modified: Wed, 10 Sep 2025 22:22:02 GMT  
		Size: 71.8 KB (71785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7783581483f58bdb451f01c59d2da525f35d38ebe491add86c7e8c95db4e138e`  
		Last Modified: Wed, 10 Sep 2025 22:22:03 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40d37a401cda0a804ab3a6687b419b7ed5f1ee3ce94f350c9ede417f6f62381`  
		Last Modified: Wed, 10 Sep 2025 22:22:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b9f3cb579fc218262f42388d3eefde9352bc0dcfe7f1acdad7b0df54f201ab`  
		Last Modified: Thu, 11 Sep 2025 00:25:10 GMT  
		Size: 218.8 MB (218786403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fca6bd34ebcd545ebabe7b22e86b16b5bd6104517d3d07db3222609a037e9a`  
		Last Modified: Wed, 10 Sep 2025 22:22:03 GMT  
		Size: 120.8 KB (120841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07370d4e2df437c088bea8a58889fbdba10f5e1784049f0edcbee3dbc252eacb`  
		Last Modified: Wed, 10 Sep 2025 22:22:03 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
