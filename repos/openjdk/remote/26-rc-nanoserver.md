## `openjdk:26-rc-nanoserver`

```console
$ docker pull openjdk@sha256:84ad688348ab0e5b9203e5281199b37872af3af78780f0a658ac56d2288239af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `openjdk:26-rc-nanoserver` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:853dad11791669eea995b8966d5f688079171d1025a30bf9d45579bdb53a5955
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.4 MB (423374163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f88542fae91124ef62cd4d9ad49b4293199724f313ae709ac9f6427b04b3f03`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 17 Feb 2026 20:05:36 GMT
SHELL [cmd /s /c]
# Tue, 17 Feb 2026 20:05:37 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 17 Feb 2026 20:05:37 GMT
USER ContainerAdministrator
# Tue, 17 Feb 2026 20:05:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 17 Feb 2026 20:05:47 GMT
USER ContainerUser
# Tue, 17 Feb 2026 20:05:48 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 20:06:15 GMT
COPY dir:48d9a1614aae77abafeeb59360dca42b580c313456033330908c8e794bbb7778 in C:\openjdk-26 
# Tue, 17 Feb 2026 20:06:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 17 Feb 2026 20:06:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf80968c83e83bc1a25677379f75f42a5bd3f0052a93e3737038836e80bb3cb4`  
		Last Modified: Tue, 17 Feb 2026 20:06:26 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2d755a02907768e1d77008be1cd86fa5db9657747f6cccd54c17e654377292`  
		Last Modified: Tue, 17 Feb 2026 20:06:26 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c34f9a0966957346ad4222101b17df008d85f8d2433e2687b1794b0a8e9971`  
		Last Modified: Tue, 17 Feb 2026 20:06:26 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1534d3a2b3df4338689780482d39f9b6084f660a085d61bbfb5448c37a5cec`  
		Last Modified: Tue, 17 Feb 2026 20:06:26 GMT  
		Size: 70.4 KB (70428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695a1d423570b9f0ad822705e891d0439e6fb126b6b76f75a450123ef58380c4`  
		Last Modified: Tue, 17 Feb 2026 20:06:24 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d232983bd9c256974ce84a9f329f8bd6253c0f15d7c4917a5e5ca809da729ce5`  
		Last Modified: Tue, 17 Feb 2026 20:06:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5605ee12b02402d666576e82a13d60735ce4c97df6fef785d7d4fb9212718482`  
		Last Modified: Tue, 17 Feb 2026 20:06:39 GMT  
		Size: 224.0 MB (223950875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f78980537ae08246d6ad5d868b1da5a403d542723617d33d3b0a0802100ec1`  
		Last Modified: Tue, 17 Feb 2026 20:06:24 GMT  
		Size: 94.8 KB (94827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50822252cce3ed7ecae40ea6d407577652b0bea603edd58405ecf17d264d5f2`  
		Last Modified: Tue, 17 Feb 2026 20:06:24 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-rc-nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:2cc308cbf67e80dea5a17180acbd82dd2c5b0a97a9bfef86018eabaa2505076c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350760684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8649cd444750a91ab6927a8761c6a75b986ed58bea461fc215499dcf397e2502`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 17 Feb 2026 20:11:58 GMT
SHELL [cmd /s /c]
# Tue, 17 Feb 2026 20:11:58 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 17 Feb 2026 20:11:59 GMT
USER ContainerAdministrator
# Tue, 17 Feb 2026 20:12:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 17 Feb 2026 20:12:13 GMT
USER ContainerUser
# Tue, 17 Feb 2026 20:12:13 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 20:13:10 GMT
COPY dir:48d9a1614aae77abafeeb59360dca42b580c313456033330908c8e794bbb7778 in C:\openjdk-26 
# Tue, 17 Feb 2026 20:13:14 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 17 Feb 2026 20:13:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9133238e3559d47b254a3443555b690c1c826f76a8aa04c2132fa0a227e81e`  
		Last Modified: Tue, 17 Feb 2026 20:13:26 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da864b46468a299f67f85f1b601d513c620a895794ef044103ead49f10b9c733`  
		Last Modified: Tue, 17 Feb 2026 20:13:26 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5310926f9234562a49802e83d7c45ae8a73c6d294e79db9ff48164c968d549a4`  
		Last Modified: Tue, 17 Feb 2026 20:13:26 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2326daa8cfc5f787121139010a5927b1505265610c4ae165b7aa5c3ffa57418`  
		Last Modified: Tue, 17 Feb 2026 20:13:26 GMT  
		Size: 71.8 KB (71819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81f2ab1289f2b20cc8011d0c0840710127db6790d0b566844506d6b0de094e6`  
		Last Modified: Tue, 17 Feb 2026 20:13:24 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3a4ca9c4d13709a447b263a4e97ab37c202561b5e1d0867023516011c3a29b`  
		Last Modified: Tue, 17 Feb 2026 20:13:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8087557568f6641a805a799768c14e8568363dacf026690779c48c7d43ad8e`  
		Last Modified: Tue, 17 Feb 2026 20:13:41 GMT  
		Size: 223.9 MB (223948930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1df0f354fa6642971a818d7ef76ff8566587f06404d1f2118150f14383cdb0`  
		Last Modified: Tue, 17 Feb 2026 20:13:25 GMT  
		Size: 87.9 KB (87874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753ccce01c4702fdef76acdc2617a8a29093968c30704271e54a366c5fb5d5bf`  
		Last Modified: Tue, 17 Feb 2026 20:13:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
