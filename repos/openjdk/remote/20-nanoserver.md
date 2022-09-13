## `openjdk:20-nanoserver`

```console
$ docker pull openjdk@sha256:d216307763e5cf1a0decd2ae911300c4fc7263502afe93a6ffd89cd920461cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `openjdk:20-nanoserver` - windows version 10.0.17763.3287; amd64

```console
$ docker pull openjdk@sha256:eb461bc2553b6a616ccd2f1d7e1de044d175cc4c59d7947a85b8979dda4fc4a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298840319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611346d5dd9f721fc2218a5c9c6fe6c629a1fe50c86f94712518e59fa98ea0aa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:57:07 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 17:00:08 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 10 Aug 2022 17:00:09 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 17:00:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Aug 2022 17:00:18 GMT
USER ContainerUser
# Mon, 12 Sep 2022 22:29:16 GMT
ENV JAVA_VERSION=20-ea+14
# Mon, 12 Sep 2022 22:29:30 GMT
COPY dir:fc970cad6b623d3dc96cba13e483a4ee274232db202104df6c8122d640a77515 in C:\openjdk-20 
# Mon, 12 Sep 2022 22:29:51 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 Sep 2022 22:29:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0f4438539876006761cb687527bd8cb94cc7a273cf8bb47563981044f2e1771e`  
		Last Modified: Wed, 10 Aug 2022 16:38:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151c855f0d179e8547473b92e962fb22b468853448fe0849dadde3526c52aceb`  
		Last Modified: Wed, 10 Aug 2022 17:28:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3386f9f9687d0a909a16379459e37c52a2de2070297d81d4167037a0602e3e86`  
		Last Modified: Wed, 10 Aug 2022 17:28:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28092505f98fc516238306cba539a3a8a6d7f48ca19dc6e6c3cca668dc6f466c`  
		Last Modified: Wed, 10 Aug 2022 17:28:35 GMT  
		Size: 75.6 KB (75615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfea14a612ecceac1dd16eaa1da4863923aa41d796fd4f9c1fae46d918d4299`  
		Last Modified: Wed, 10 Aug 2022 17:28:33 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b505f4434e2e6765bfce70588d7f046bcc13a28782ba51a392e7241581ed9496`  
		Last Modified: Mon, 12 Sep 2022 22:33:32 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1711a40a31f07fbb060dffd661d6381baee9727057050e6fedab890217b6eca6`  
		Last Modified: Mon, 12 Sep 2022 22:33:51 GMT  
		Size: 191.8 MB (191818966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064de83d09f7764a7f9dc01022bb4159a7d3665969f1015f0c71619cab1bad04`  
		Last Modified: Mon, 12 Sep 2022 22:33:33 GMT  
		Size: 3.7 MB (3734689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c86c759b7fcf496f001c5d5b2cf9c657e0d3a4670e1ffeaaccd28a045796e6`  
		Last Modified: Mon, 12 Sep 2022 22:33:32 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
