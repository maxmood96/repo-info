## `openjdk:26-ea-14-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:06aba085be1bcaf14f6ee72de8fcb4837d96b33a9781569560265f864431cf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-14-jdk-nanoserver` - windows version 10.0.26100.6584; amd64

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

### `openjdk:26-ea-14-jdk-nanoserver` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:a9a8eb9e0250cd2025a4fd6644173892f96c66a0cce207d16aa39699c91544c0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341736751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bc7b405a2211f6c443a3944815a03354a6a3e4a57b1c3b3c1b92cbfcf8b22d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:19:27 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:21:06 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 10 Sep 2025 22:21:07 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:21:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Sep 2025 22:21:09 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:21:10 GMT
ENV JAVA_VERSION=26-ea+14
# Wed, 10 Sep 2025 22:21:40 GMT
COPY dir:d50107523f417125c2242d5366bf04295424e0a959b88dfcf6f8074b4fb0cc43 in C:\openjdk-26 
# Wed, 10 Sep 2025 22:21:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Sep 2025 22:21:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9a238b296b863260af62360805baa85f9d2fb272823e764b654e58032e367a`  
		Last Modified: Wed, 10 Sep 2025 23:08:42 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f090545af493136aaff79babf145490f923a2bdd50029ac5ee0a7186dd447b36`  
		Last Modified: Wed, 10 Sep 2025 22:22:31 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11693c159ac41721b77f00a946a65f19157d846f76af5234ecbea8df8b02a516`  
		Last Modified: Wed, 10 Sep 2025 22:22:31 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73854d2d6cebe20bdcf587664bb7516ccac951124877d5aaf3387ec1ba54dc3`  
		Last Modified: Wed, 10 Sep 2025 22:22:31 GMT  
		Size: 76.5 KB (76471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9c12ab36c3ddafd637da6ed02710756965f8db8ad5118cea76d6e55f27ecff`  
		Last Modified: Wed, 10 Sep 2025 22:22:32 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2761bf0c315d7fd00f15796a9d448c1c34a910ea27710c06caad51446ad3563`  
		Last Modified: Wed, 10 Sep 2025 22:22:32 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9299124a176285a747c423f15972955efea691186e1d1f39b4032b20b4009011`  
		Last Modified: Thu, 11 Sep 2025 00:26:21 GMT  
		Size: 218.8 MB (218786193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7011946b3e8e62e4d47a154b977a395ddf06a64433cb6c781a66d5b931e670`  
		Last Modified: Wed, 10 Sep 2025 22:22:32 GMT  
		Size: 147.8 KB (147789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfb4a8469ea5759484916af1ee1c916f42ebf7f58807dd49189fb4954a19693`  
		Last Modified: Wed, 10 Sep 2025 22:22:32 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
