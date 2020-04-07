## `openjdk:15-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:426dad6b1bf40500682366f14a65633a112dc42e66254543f115a94e39d36faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `openjdk:15-ea-nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:e3cf7ca7ae71a5af6c9d18c9c3a10bed7bd4dbbe2d28202fbc392da99d364b2c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297930846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56aeaf711e03d9d27504e0293ad3305a7528052c09e16709e8bc7d64cfaf1aed`
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
# Mon, 06 Apr 2020 23:20:26 GMT
ENV JAVA_VERSION=15-ea+17
# Mon, 06 Apr 2020 23:21:16 GMT
COPY dir:9900238beb32222ff35464f359081668372e466ea0960b63b07f741979ff5e5f in C:\openjdk-15 
# Mon, 06 Apr 2020 23:21:37 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Mon, 06 Apr 2020 23:21:38 GMT
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
	-	`sha256:1f873aba5d8443b96f056747b90d094be00c9e75f7598aae9f6edc48da16f061`  
		Last Modified: Mon, 06 Apr 2020 23:26:43 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0d33a8aacb82e90569fb7f27d550e9a3e418acf91595b77ccc571666ae5aa5`  
		Last Modified: Mon, 06 Apr 2020 23:27:03 GMT  
		Size: 193.3 MB (193346868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6a2d9538e9c78b3d0a19cd3cdb348bb100c5729ffd75e2c61aedce966f7381`  
		Last Modified: Mon, 06 Apr 2020 23:26:46 GMT  
		Size: 3.5 MB (3461075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045aca2a29ecff619e13c876b7cbbd85c9ef6017f66c2b3cc04911d2a7008d54`  
		Last Modified: Mon, 06 Apr 2020 23:26:42 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
