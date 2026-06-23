## `openjdk:28-ea-nanoserver`

```console
$ docker pull openjdk@sha256:66658e68cee644f49388389b68384302f48531e3e12a6d7bfd01ed831c848a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `openjdk:28-ea-nanoserver` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:e7d6a76809850674a71680cdf9b67a50e66c4c33788da0ab5ccaff7e03b272c3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.9 MB (420875817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8601bb227c497daf622fbf8206d1ede0f7beda0fbbee38bbd245c78bc4c85b6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Mon, 22 Jun 2026 23:09:35 GMT
SHELL [cmd /s /c]
# Mon, 22 Jun 2026 23:09:35 GMT
ENV JAVA_HOME=C:\openjdk-28
# Mon, 22 Jun 2026 23:09:36 GMT
USER ContainerAdministrator
# Mon, 22 Jun 2026 23:09:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 22 Jun 2026 23:09:46 GMT
USER ContainerUser
# Mon, 22 Jun 2026 23:09:47 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 23:10:11 GMT
COPY dir:143aad653eaf1eafb22a0522125924463ceb107c7fe7f919363f4a6a05e7f3be in C:\openjdk-28 
# Mon, 22 Jun 2026 23:10:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 22 Jun 2026 23:10:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834926281133e5abf1c51b7351f9fab8669b188e96d89bb4f19538466966cdc8`  
		Last Modified: Mon, 22 Jun 2026 23:10:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96646fd92a05557bfda2ae7665775c141670345ca00efc83bc6ddf425fffbc61`  
		Last Modified: Mon, 22 Jun 2026 23:10:27 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5852b366286c3a136d5602fe22598d056674e117ae9cf96d9a91f33606543cb3`  
		Last Modified: Mon, 22 Jun 2026 23:10:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453cbcc2746dc57efc4e6e76f6955f54166a5c1c1dd7cdfe6d18193d5f48cb52`  
		Last Modified: Mon, 22 Jun 2026 23:10:27 GMT  
		Size: 70.6 KB (70573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0c1d980cafa3ec8b165b74371b2aafdc5c426b2c33a2cea38a9a6629c1072b`  
		Last Modified: Mon, 22 Jun 2026 23:10:25 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf82044cc1dd649d151090deb393e3831991848acc1bbae558987efd4efeeda1`  
		Last Modified: Mon, 22 Jun 2026 23:10:25 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32087660bf608303cd5f1dd2c863f76a23cedcdf129e7bebf28959b2758344dd`  
		Last Modified: Mon, 22 Jun 2026 23:10:39 GMT  
		Size: 224.0 MB (224028221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7899daed09ff2913dec337190608a6bbcf6572f6ba67885428df3af99e8bd167`  
		Last Modified: Mon, 22 Jun 2026 23:10:25 GMT  
		Size: 102.7 KB (102686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44b4cf6e42c5e1d26a1bdda7cc06a4ef06e318b0690a22ee4814edcdd669435`  
		Last Modified: Mon, 22 Jun 2026 23:10:25 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:28-ea-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:a6b991a751181a36434ac98ca408d5b4dd46e35037992a7a17b988930f041275
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.2 MB (348228700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71fac6b4bdaed7b95bf82c0cfc71b10e70c760e669874b3ef695cdf410d297a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 22 Jun 2026 23:09:38 GMT
SHELL [cmd /s /c]
# Mon, 22 Jun 2026 23:09:39 GMT
ENV JAVA_HOME=C:\openjdk-28
# Mon, 22 Jun 2026 23:09:39 GMT
USER ContainerAdministrator
# Mon, 22 Jun 2026 23:09:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 22 Jun 2026 23:09:48 GMT
USER ContainerUser
# Mon, 22 Jun 2026 23:09:48 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 23:10:25 GMT
COPY dir:143aad653eaf1eafb22a0522125924463ceb107c7fe7f919363f4a6a05e7f3be in C:\openjdk-28 
# Mon, 22 Jun 2026 23:10:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 22 Jun 2026 23:10:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba0f432fefafc0c6fd12b6a284baaf7ebad1126900fe4bd8e80b86cbfeec188`  
		Last Modified: Mon, 22 Jun 2026 23:10:38 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f763f86199e7fecea7036cc9a2bf10ec901e80b69888dab684009b290c62bf`  
		Last Modified: Mon, 22 Jun 2026 23:10:38 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f4b940a3c76db9df0c142dbccbf2c3ecf63b463d1a12134fa571950ed73eac`  
		Last Modified: Mon, 22 Jun 2026 23:10:38 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a61893a4c03135238dc99f412c8f35d362e6d8867bf459de319c9b19a3a8712`  
		Last Modified: Mon, 22 Jun 2026 23:10:38 GMT  
		Size: 73.4 KB (73393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779739fee8f7ed720829e2d93cb1d2ab9600075872f343f6af6704518ae7ae79`  
		Last Modified: Mon, 22 Jun 2026 23:10:36 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d7e9cf933fd6594e42330339a5cd3e7a0921caa0b1c4b0860f6776ad23b6f1`  
		Last Modified: Mon, 22 Jun 2026 23:10:36 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232c7d1ec9fb9570189a1e2f11b0d5efc521b54e3a036fcb788f8f12bfbea140`  
		Last Modified: Mon, 22 Jun 2026 23:10:52 GMT  
		Size: 224.0 MB (224028648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d705877710ee6172d7a99879bc32ca8f5305b23dea397e2d7142706dc107f9`  
		Last Modified: Mon, 22 Jun 2026 23:10:36 GMT  
		Size: 122.8 KB (122781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26b04c3d5e5925554f99bd5bc4fff95b40f3fb39d4f6da1303645cc1511b119`  
		Last Modified: Mon, 22 Jun 2026 23:10:36 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
