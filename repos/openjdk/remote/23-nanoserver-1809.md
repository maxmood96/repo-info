## `openjdk:23-nanoserver-1809`

```console
$ docker pull openjdk@sha256:f9e8cd7167a80f032e7dcd54259ef7a5ef00f96b22b00c3b9edd789957c4bd14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:ecd2c7341c1ddf9321b56f8942d3d88806bc0d1892c36e7adbec4a76b328f958
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.4 MB (366430766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e104404cfa0188e911442cf52635773dc660f0d3ea4f0acb8c0362b9a601efb6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Fri, 12 Jul 2024 23:09:31 GMT
SHELL [cmd /s /c]
# Fri, 12 Jul 2024 23:09:32 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 12 Jul 2024 23:09:33 GMT
USER ContainerAdministrator
# Fri, 12 Jul 2024 23:09:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 12 Jul 2024 23:09:36 GMT
USER ContainerUser
# Fri, 12 Jul 2024 23:09:37 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 23:09:45 GMT
COPY dir:b28b06e2874a54ae1be3be2ef41ab0d3cda7f2ba53f80bc65a31a690196cce90 in C:\openjdk-23 
# Fri, 12 Jul 2024 23:09:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 12 Jul 2024 23:09:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795a659bdf5bffe9aaeeee8046885dbcf81ac1a1a866aa9727ba37c455f17830`  
		Last Modified: Fri, 12 Jul 2024 23:09:57 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4579c46b900a85629c87237e570dd37f9e9aaa0a34f159276eda7b5a63c460c6`  
		Last Modified: Fri, 12 Jul 2024 23:09:57 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7175ee09f818fe7c7d0ca015d741c6c1841deddbe19eaba38cdf7241ce8d88fe`  
		Last Modified: Fri, 12 Jul 2024 23:09:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f994bb6527754637d3b32ae974018c1da89ddfc4d7c2d61b37e1a8f53eaf5ec`  
		Last Modified: Fri, 12 Jul 2024 23:09:56 GMT  
		Size: 73.0 KB (73018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac6094d95216dc79373d02b0f902d321d67e87109587cb652bcb74135d2b45b`  
		Last Modified: Fri, 12 Jul 2024 23:09:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd27fcf93cd2182291231152e745ed03e79f37d1d348ed7671d9f8dc724400a9`  
		Last Modified: Fri, 12 Jul 2024 23:09:56 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bc13e23bf43d3a8e03aad216883ea99b9effe3e80adcf5c8e426ed069cbcc0`  
		Last Modified: Fri, 12 Jul 2024 23:10:07 GMT  
		Size: 206.1 MB (206056717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9976e5a2de6a20736ffc7b5cddba12ffc0a0e630022244a4f1ed4efd7a786c`  
		Last Modified: Fri, 12 Jul 2024 23:09:56 GMT  
		Size: 5.2 MB (5213402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d869274c112fc7003f8f4399788905223ac1f3706e36f9616c4e031ea9ba6c`  
		Last Modified: Fri, 12 Jul 2024 23:09:56 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
