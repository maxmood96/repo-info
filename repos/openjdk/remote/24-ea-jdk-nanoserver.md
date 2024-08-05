## `openjdk:24-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:cf7bc22f7180e5782d155a5ee72e566f0614c1ea6ef1c8c86b93543db0edf319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:24-ea-jdk-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:dbc834755fa2af1f477898b10f5f528b1c7eedcf269b77e3b0f00a081ef55c74
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.8 MB (365768196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8172fafe73eb1c9bd690197b73b0689ee96fe1656d23138bde101503a0b499f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Mon, 05 Aug 2024 19:52:36 GMT
SHELL [cmd /s /c]
# Mon, 05 Aug 2024 19:52:37 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 05 Aug 2024 19:52:38 GMT
USER ContainerAdministrator
# Mon, 05 Aug 2024 19:52:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 05 Aug 2024 19:52:43 GMT
USER ContainerUser
# Mon, 05 Aug 2024 19:52:44 GMT
ENV JAVA_VERSION=24-ea+9
# Mon, 05 Aug 2024 19:52:52 GMT
COPY dir:2a893fddde06126611c847c0c8a5235c5e193fdfb586914db4687f7c9473d2e4 in C:\openjdk-24 
# Mon, 05 Aug 2024 19:52:57 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 05 Aug 2024 19:52:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d082ed38cec69b2ab4bf4c6f14eafdb3b291eda1cdb4c8ab74a79423d667241`  
		Last Modified: Mon, 05 Aug 2024 19:53:05 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adac57b78d07e2ee1a2056a58d18d4ea3860c418cf3534cdf6e5e1f212a30a1`  
		Last Modified: Mon, 05 Aug 2024 19:53:04 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0500801d5979e8c747837a27a7d894529878ece0259f246581aa9dc552c9c2ed`  
		Last Modified: Mon, 05 Aug 2024 19:53:04 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a76dfaf72537cdc70910c37e252c333d3f4505cb514504087cd3f00c20b1be4`  
		Last Modified: Mon, 05 Aug 2024 19:53:05 GMT  
		Size: 67.8 KB (67802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e5bd0adfb7721b6666451e16930425cc0e177a2fc0e7beae525e2aa23b94b6`  
		Last Modified: Mon, 05 Aug 2024 19:53:02 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dad6facd19667150a1facf8bef230c00a0f7d1851cca3bafedb6149a76f8c3`  
		Last Modified: Mon, 05 Aug 2024 19:53:03 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0704b6d9624b611786fde95db8bdab3dddd67189434025d785d36353f4b2b6d7`  
		Last Modified: Mon, 05 Aug 2024 19:53:13 GMT  
		Size: 206.5 MB (206531521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9811dffdbc86117b331b9cd97dedf54ffda836ebfddf47aa31c6eca30937c3a`  
		Last Modified: Mon, 05 Aug 2024 19:53:03 GMT  
		Size: 4.1 MB (4081019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a270897b2e15ea605b4ecaaf0f60d40dc35e51928e34cecfbce4f1b3576f3a`  
		Last Modified: Mon, 05 Aug 2024 19:53:02 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
