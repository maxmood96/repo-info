## `openjdk:24-ea-33-nanoserver`

```console
$ docker pull openjdk@sha256:8cf8ff221b802f8ccdf4762a944441ecbe90c8399aca06f80ba43dcb9b3c94f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-33-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:bcf8b01a54764b075bfccbfb1b0ca8f6b7e08b4a622e0b5ba4028757c3d8d7b8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407719326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7c4cba251fbb2e166225f79e4abec8c128f821a2ac6735b9aa8f261127fd2d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 29 Jan 2025 01:32:19 GMT
SHELL [cmd /s /c]
# Wed, 29 Jan 2025 01:32:20 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 29 Jan 2025 01:32:21 GMT
USER ContainerAdministrator
# Wed, 29 Jan 2025 01:32:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Jan 2025 01:32:27 GMT
USER ContainerUser
# Wed, 29 Jan 2025 01:32:29 GMT
ENV JAVA_VERSION=24-ea+33
# Wed, 29 Jan 2025 01:32:36 GMT
COPY dir:0501e586ce21e14cfb645b0134706225edb213a038c5d5da062ef05b40a90877 in C:\openjdk-24 
# Wed, 29 Jan 2025 01:32:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Jan 2025 01:32:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbb17a334e2267dfe34c8a6e200b6502ad432dd0919391b20a2f30b5ff78c90`  
		Last Modified: Wed, 29 Jan 2025 01:32:52 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d8e560c3709e0fc7b9a087928022003bc163ef5293433a7ef6af2ce24ffb96`  
		Last Modified: Wed, 29 Jan 2025 01:32:52 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d858a86d10254d90e4bb3d00c0e799a7f71649e8d2bdcbd142e3120808ebcf`  
		Last Modified: Wed, 29 Jan 2025 01:32:52 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c87c9944bd1bccafabf2c3acded582f324980aae928064f537f3548f8f126`  
		Last Modified: Wed, 29 Jan 2025 01:32:52 GMT  
		Size: 75.4 KB (75440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7038b340b796648be80e40ba746d0ac585f591a90c3f20e03b9bbffd4a4279`  
		Last Modified: Wed, 29 Jan 2025 01:32:51 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a2abb6b5b71edc0f89e02a40284bf895e1d83159a3c4b22492a7d667c004c1`  
		Last Modified: Wed, 29 Jan 2025 01:32:51 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8fa42baa1d2b21660c2a6164114a089b3ef60062e8353201a7f06bfe4649c5`  
		Last Modified: Wed, 29 Jan 2025 01:33:03 GMT  
		Size: 208.5 MB (208491486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7870d8d078737bb1cfb4e21816993c67032d8f698865a56f3c3a1dcdb623127`  
		Last Modified: Wed, 29 Jan 2025 01:32:51 GMT  
		Size: 91.7 KB (91709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e98bd40113562c1cca0bba0356b666482b9d771ba53ca88a2570af2f6b12aab`  
		Last Modified: Wed, 29 Jan 2025 01:32:51 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-33-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:1571a67582a97f09bc2f5b06ff6c5903382aeed848fcf2276dfe2d8954013dcf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.3 MB (329329203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138122080a16c14c826ab63e1fab751de0f25928cd14070feed375b0c9f8e580`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 29 Jan 2025 00:27:23 GMT
SHELL [cmd /s /c]
# Wed, 29 Jan 2025 00:27:23 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 29 Jan 2025 00:27:24 GMT
USER ContainerAdministrator
# Wed, 29 Jan 2025 00:27:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Jan 2025 00:27:41 GMT
USER ContainerUser
# Wed, 29 Jan 2025 00:27:42 GMT
ENV JAVA_VERSION=24-ea+33
# Wed, 29 Jan 2025 00:27:50 GMT
COPY dir:0501e586ce21e14cfb645b0134706225edb213a038c5d5da062ef05b40a90877 in C:\openjdk-24 
# Wed, 29 Jan 2025 00:27:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Jan 2025 00:27:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f474b7bed30e00264915468de818bd74c81954bfa7355b352339f778f9c2e97`  
		Last Modified: Wed, 29 Jan 2025 00:28:00 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6486392f9c67365da516dd7b1723a161d1f6ad9c553d8970c1cc9a969d05bf81`  
		Last Modified: Wed, 29 Jan 2025 00:28:00 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca3ec4012effeb63c54c082b2abac4988ceae880a6e59d4d81fc5a6c44f47ed`  
		Last Modified: Wed, 29 Jan 2025 00:28:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042a3d0ba736a308885dc6b28d1c5d5dcd347ab924b3302d67ca0e5b923c38ac`  
		Last Modified: Wed, 29 Jan 2025 00:28:00 GMT  
		Size: 73.1 KB (73141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7ee19f22d1bc62fa3ca860edfdbcda897556525501fb1f90341da45f1dc099`  
		Last Modified: Wed, 29 Jan 2025 00:27:59 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efe0c8ee6e229c038e3978c9c5114df6f093c1a68c8acfb3c5fbdbd7c9746e8`  
		Last Modified: Wed, 29 Jan 2025 00:27:59 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea799b9e89ed3411b70022dd81037eb25ee11da90a07a7057432a7484d40311`  
		Last Modified: Wed, 29 Jan 2025 00:28:10 GMT  
		Size: 208.5 MB (208490453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c80ad46b46d05131eebffead2aab8bd65fa453a163d1ba92c0d39d36d63877`  
		Last Modified: Wed, 29 Jan 2025 00:27:59 GMT  
		Size: 97.8 KB (97842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcf37ee1900462cdd9f897619bc9afd55598345310409f5ac6f851b435dcac4`  
		Last Modified: Wed, 29 Jan 2025 00:27:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-33-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:69464fe0d6aec1374c7591dacc3e10b67a425b9f52a4d153895db5c166ba3cc5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368215579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc27a7c1ad6073b506e0708feb0e209ea3eef82a72d60183c25f37bf59f30c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 29 Jan 2025 01:28:28 GMT
SHELL [cmd /s /c]
# Wed, 29 Jan 2025 01:28:30 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 29 Jan 2025 01:28:31 GMT
USER ContainerAdministrator
# Wed, 29 Jan 2025 01:28:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Jan 2025 01:28:49 GMT
USER ContainerUser
# Wed, 29 Jan 2025 01:28:49 GMT
ENV JAVA_VERSION=24-ea+33
# Wed, 29 Jan 2025 01:29:03 GMT
COPY dir:0501e586ce21e14cfb645b0134706225edb213a038c5d5da062ef05b40a90877 in C:\openjdk-24 
# Wed, 29 Jan 2025 01:29:09 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Jan 2025 01:29:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47f657c1b441b831e252022f38eb928e1b466db37be2bec78c6ce54f9889a49`  
		Last Modified: Wed, 29 Jan 2025 01:29:14 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67de9982c926acf1ab99924b9e2630194cc4b2a4bd8b75d082db836dac0bd48`  
		Last Modified: Wed, 29 Jan 2025 01:29:14 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0565120c5e75b8617ce753dde25f7c5b2529b3c8b1d455e760d12990567ae4b0`  
		Last Modified: Wed, 29 Jan 2025 01:29:14 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ceae1f7599d8e2aa14635d0dc5b6a5204b61ff77c888402a5896336d08709`  
		Last Modified: Wed, 29 Jan 2025 01:29:14 GMT  
		Size: 67.8 KB (67770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d7d32ef6426bb73f8aeb780e1e71d74bdf0032d11a6625534fe443ac6c255b`  
		Last Modified: Wed, 29 Jan 2025 01:29:13 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b24efd1519f763869319b98c0d7af54d4a2bfbbc65b66cf868a237ef7bbe77`  
		Last Modified: Wed, 29 Jan 2025 01:29:13 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151ffc6437a9734cd20fb9ad869447c73cdc2c746ce51b5c723945af93e6dcca`  
		Last Modified: Wed, 29 Jan 2025 01:29:24 GMT  
		Size: 208.5 MB (208491130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3e63e334bb48d10a63aac04ea32a4a8a35252592999edde3e7f7ccc8c9bc9c`  
		Last Modified: Wed, 29 Jan 2025 01:29:13 GMT  
		Size: 4.4 MB (4382728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d0e4eee5840a3caaf03774d430b2f7d090c8f09575b19cc1f0a56967ae7b3a`  
		Last Modified: Wed, 29 Jan 2025 01:29:13 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
