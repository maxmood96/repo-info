## `openjdk:15-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:c1fded26b408e597dbf576aa913cd6da32fd0f299fd717ec0708c5eabf9bf7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `openjdk:15-jdk-nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:b949be92816eb265feb5b35c3f5aa4905f352d72948ce3adc816bfabaefc9db0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297919342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ae6b3729c7b0d032d632a0fff24708e2727763f6ac683b4823c4844c1185f0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:56:25 GMT
SHELL [cmd /s /c]
# Wed, 11 Mar 2020 14:56:27 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 11 Mar 2020 14:56:28 GMT
USER ContainerAdministrator
# Wed, 11 Mar 2020 14:56:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Mar 2020 14:56:55 GMT
USER ContainerUser
# Tue, 31 Mar 2020 00:22:48 GMT
ENV JAVA_VERSION=15-ea+16
# Tue, 31 Mar 2020 00:23:36 GMT
COPY dir:b8c5e0ce3933eceb7ab965f53d3634117b5e48dcb9defbeef7656d883d255a5d in C:\openjdk-15 
# Tue, 31 Mar 2020 00:23:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Tue, 31 Mar 2020 00:23:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a66be005a5120fc8bbc31290c77aa0e6580d02bc61948ef0602bf09a6ab61ba`  
		Last Modified: Wed, 11 Mar 2020 15:26:11 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa222a675c58ae4e16af815d117d614899889b99615416d258fea25600f704cc`  
		Last Modified: Wed, 11 Mar 2020 15:26:08 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca058e8ce192a6fd627d0c85ec3d6b2843d8adc7b0a24db65d4460a1388d514`  
		Last Modified: Wed, 11 Mar 2020 15:26:08 GMT  
		Size: 934.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adfe4646dd92a1ea69c4f00cecd622a93c1467830cd992635a0ba3bc689db93`  
		Last Modified: Wed, 11 Mar 2020 15:26:08 GMT  
		Size: 67.2 KB (67155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5348a60ea8643e6600613c06514ce34cb7bf596bd992df4b5f09a9e3b9226f76`  
		Last Modified: Wed, 11 Mar 2020 15:26:04 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892782ca4dac4b30090ad224fff0bd9a7cd65f42d72800a469030f0eae1c037a`  
		Last Modified: Tue, 31 Mar 2020 00:28:40 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce1fdf5c3ff84bcec5b66b3a3cbf74fca097689f9999cfb310f47dc35951170`  
		Last Modified: Tue, 31 Mar 2020 00:28:58 GMT  
		Size: 193.3 MB (193337063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70683dd73470633d0b9b41b6267c262b91a40c91c6cc18ee93a625eb654f7a8`  
		Last Modified: Tue, 31 Mar 2020 00:28:41 GMT  
		Size: 3.5 MB (3459324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b568757b475fa1379e46bbbd352f615084abde6c3177fc12f6904e86c581b3b4`  
		Last Modified: Tue, 31 Mar 2020 00:28:40 GMT  
		Size: 911.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
