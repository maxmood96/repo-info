## `openjdk:20-nanoserver`

```console
$ docker pull openjdk@sha256:eeb590a335a1b72811435c5cb855280f5ab593d5d1b346eac2c148637f8a335f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `openjdk:20-nanoserver` - windows version 10.0.17763.3046; amd64

```console
$ docker pull openjdk@sha256:97936e0b3728de0c010bef6f8c901c5c44156f872e0d08c4f67a5806de61c9d7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 MB (299167491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08d7596a8db53d6f17c89db9b0ceb9899537aca74ecd7991340f9f4f822b402`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 17:30:58 GMT
SHELL [cmd /s /c]
# Thu, 16 Jun 2022 01:19:36 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 16 Jun 2022 01:19:37 GMT
USER ContainerAdministrator
# Thu, 16 Jun 2022 01:19:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Jun 2022 01:19:50 GMT
USER ContainerUser
# Tue, 28 Jun 2022 00:18:18 GMT
ENV JAVA_VERSION=20-ea+3
# Tue, 28 Jun 2022 00:18:33 GMT
COPY dir:4fac57c11e3c85ab1eca1275cd64e623770c0db7cf95f3962cc150cc0f07e33d in C:\openjdk-20 
# Tue, 28 Jun 2022 00:18:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 28 Jun 2022 00:18:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92b4c385cd5cbb12fb09cb31c12b5e5de38cf7b380c8681286caac242c06d3ed`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda95a4aa1ce8b324ff84e1ccdf8befbe50e58a948d31b65618925e2842efada`  
		Last Modified: Thu, 16 Jun 2022 01:33:30 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f66084dce2c5c1fa8b13cd8edb172b48a4411ebf5466035c9c5fef517796cce`  
		Last Modified: Thu, 16 Jun 2022 01:33:30 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a225993ae008c14a2ad71f55edbcafc99d581fba5b2fd8297a2af9bd6fc2d`  
		Last Modified: Thu, 16 Jun 2022 01:33:30 GMT  
		Size: 71.2 KB (71215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1582199825c588de3fcfbec196a74a70813b8a78abaa2abbed131795de8f1d6`  
		Last Modified: Thu, 16 Jun 2022 01:33:27 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6345e8a68a1bb234c1769c6f6457df34b61f2c01a4f59091d10c1a18ace049`  
		Last Modified: Tue, 28 Jun 2022 02:21:52 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055d6a4af64d9aabcb07782660f5cdca11dce3b2fb1e27ec2e66d61d50a34191`  
		Last Modified: Tue, 28 Jun 2022 02:25:21 GMT  
		Size: 192.2 MB (192205578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523ef644785146d7ab0ac19979a3595aec16b329124494039933447452ce3360`  
		Last Modified: Tue, 28 Jun 2022 02:21:56 GMT  
		Size: 3.7 MB (3730545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a39f70c665105c4229f9aca50ec36314ce8b48f804e05483b2a7a5ddca90917`  
		Last Modified: Tue, 28 Jun 2022 02:21:52 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
