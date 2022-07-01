## `openjdk:20-ea-nanoserver`

```console
$ docker pull openjdk@sha256:d2cccf41840197ea1f740baba9b0c82e718ee7394d9f6339a86431f084812cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `openjdk:20-ea-nanoserver` - windows version 10.0.17763.3046; amd64

```console
$ docker pull openjdk@sha256:0b465dfcfcba76b6c6b321b0b86934b69cd426ba36120b4893a2cb1a7fb32530
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298718799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef6831e6f4d2e38dff5be773551745837d5c5c6430d5f9819790581fdf2c7d4`
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
# Fri, 01 Jul 2022 01:19:17 GMT
ENV JAVA_VERSION=20-ea+4
# Fri, 01 Jul 2022 01:19:33 GMT
COPY dir:909ba4131f169bb5993ae4f7488a319df903505bd680c2d45204109f32734278 in C:\openjdk-20 
# Fri, 01 Jul 2022 01:20:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 01 Jul 2022 01:20:04 GMT
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
	-	`sha256:60dcdffa5f5ab6a3bfd04521a7d38a9cacbf3885a4ede107ee70cd392498f298`  
		Last Modified: Fri, 01 Jul 2022 01:37:28 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37440a354d1a56f2d2a52dee0b93b15d6beb3e96d9d0bdeb783bfe8849b91667`  
		Last Modified: Fri, 01 Jul 2022 01:40:58 GMT  
		Size: 191.8 MB (191759289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56ccfc765a1cd6a772f9d8cbaa3052127c91bf77949fa85ff0cfc74d714305d`  
		Last Modified: Fri, 01 Jul 2022 01:37:32 GMT  
		Size: 3.7 MB (3728114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce855bdc46adbbe855e30fbea314d72fca475e75aaf9ad8236fbf3f87dc9ca6`  
		Last Modified: Fri, 01 Jul 2022 01:37:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
