## `openjdk:nanoserver`

```console
$ docker pull openjdk@sha256:9fbb14ed2c459dc93015a0d2389547abdb048fc436b53340518a712f29a91d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `openjdk:nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull openjdk@sha256:0b386c6d526bf0960310da6254fa9a6835e1bb4948220114c4caabc5b696291c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294714530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ded6d05c44a03f636340ab089a115483f3f218ed25b32aebb7853e254f2dfab`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Tue, 08 Nov 2022 18:36:25 GMT
SHELL [cmd /s /c]
# Wed, 09 Nov 2022 17:33:02 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 09 Nov 2022 17:33:03 GMT
USER ContainerAdministrator
# Wed, 09 Nov 2022 17:33:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Nov 2022 17:33:18 GMT
USER ContainerUser
# Wed, 09 Nov 2022 17:33:19 GMT
ENV JAVA_VERSION=18.0.2.1
# Wed, 09 Nov 2022 17:33:35 GMT
COPY dir:ee5a32dc618f3d1ccd1a23fd44bf5e8d063a799e660c0fa7a176452c3ac100ba in C:\openjdk-18 
# Wed, 09 Nov 2022 17:33:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 09 Nov 2022 17:33:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e8f4bb4b79b67857c1e4ac5c66026fd5ff5badbde5a8b59b11251b02699586`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5f98edd9feb4c915b2f5cefd45fbd917ae08e3bf8f01df18b914a85abc62bf`  
		Last Modified: Wed, 09 Nov 2022 17:39:45 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83753fad4f9bd2fe907a088b31b10b87ede6de16504750e31017219ee25c355d`  
		Last Modified: Wed, 09 Nov 2022 17:39:44 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c1821ea531880b41a2d0d3ef6d40d7600f2cf5e742ffd9f7b5d30dc2975bba`  
		Last Modified: Wed, 09 Nov 2022 17:39:44 GMT  
		Size: 67.5 KB (67502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b4316e6cb59ab38a194342891de49dc7d479c526280e44f84a43b834cbd0fa`  
		Last Modified: Wed, 09 Nov 2022 17:39:42 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b539fa9bf4554d59ebd64aa1f5f0ef2b3b514dd5f235686b6cf5ab944dfcf777`  
		Last Modified: Wed, 09 Nov 2022 17:39:42 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d3881a0168db1cd3f83736a26fbba06f99e5d38080515492ebc2bafaed6cbb`  
		Last Modified: Wed, 09 Nov 2022 17:40:04 GMT  
		Size: 184.3 MB (184349912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9caef852039f8d4b6eebad7abb8b467e51202f0c0651f2565f904120fd7861`  
		Last Modified: Wed, 09 Nov 2022 17:39:43 GMT  
		Size: 3.6 MB (3566841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb47213c0db62272c4b349f83ec6c2bc4014db272ae3741627f7a9d6fc552b15`  
		Last Modified: Wed, 09 Nov 2022 17:39:42 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
