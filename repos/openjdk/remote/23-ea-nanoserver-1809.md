## `openjdk:23-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:473fc169bf928d7876ad1db1e606df01aaff196d0efcb93185f3a1b5bf3b307e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-ea-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:1ccc15ad6e6a90764224cd770a8440e7d8d8c3a57d9d3ffc782069099e5ab118
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307306127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad902aefc2df7d56c96b720f70643029560ff7510c1d0219888ca51168f97174`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Mon, 25 Mar 2024 20:12:15 GMT
SHELL [cmd /s /c]
# Mon, 25 Mar 2024 20:12:16 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 25 Mar 2024 20:12:17 GMT
USER ContainerAdministrator
# Mon, 25 Mar 2024 20:12:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 25 Mar 2024 20:12:26 GMT
USER ContainerUser
# Mon, 25 Mar 2024 20:12:27 GMT
ENV JAVA_VERSION=23-ea+15
# Mon, 25 Mar 2024 20:12:37 GMT
COPY dir:7ce79fe08d9fec44f12de59ee3f032b62a522e136b44f93fd6c147c77463a7c8 in C:\openjdk-23 
# Mon, 25 Mar 2024 20:12:50 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 25 Mar 2024 20:12:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8543b40c855b6019291d7d809014792a528c62912601593372417033f766b2f5`  
		Last Modified: Mon, 25 Mar 2024 20:12:59 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3959964baedd11db33f34ef9176767b1658ad92124ff8e9b2917d3ec44c57104`  
		Last Modified: Mon, 25 Mar 2024 20:12:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f1d22320d513b7df545cf88766ed9ee65b107479d3e4dfea88c03fb580f05a`  
		Last Modified: Mon, 25 Mar 2024 20:12:57 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f712d827ad60d2654b250c28db35ed391075e19a849481b00b8dafd1ae2d072`  
		Last Modified: Mon, 25 Mar 2024 20:12:57 GMT  
		Size: 65.8 KB (65765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19461ac3269c0c4bb15e8d008b5f8a8fa8a27ab446b46e91d2f80ff464438696`  
		Last Modified: Mon, 25 Mar 2024 20:12:56 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c986c26aaccecb8881e45aa414aa603ab08052062583b16c30490ac4fb39f61`  
		Last Modified: Mon, 25 Mar 2024 20:12:56 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749fb67e13c9c579e24616d56c39b8b5d085f58a5e027d71a3e29cacc6649c68`  
		Last Modified: Mon, 25 Mar 2024 20:13:07 GMT  
		Size: 197.2 MB (197160369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69268eedb22d409184d0d5e37f4dca749bb606ec4034e0eaeb6e91a03a7eb596`  
		Last Modified: Mon, 25 Mar 2024 20:12:57 GMT  
		Size: 5.5 MB (5453605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9440e9b56ac534d85c550ad27d2569a993168e41dc42309364e1bc3c82ea66`  
		Last Modified: Mon, 25 Mar 2024 20:12:56 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
