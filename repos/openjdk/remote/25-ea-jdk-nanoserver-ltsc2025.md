## `openjdk:25-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:23078a8986f7591688a1783ca0762a5ab261384676ca2b760af11348808f4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:64d207c66299f4dc0da767fe2f1e562329d4fba01640815ffa3a4e05b972f4f1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.1 MB (410053765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1305174f77fc3cf74fcb2f2d746110ae42d948574c3a9d333ba4da8f4da2be0d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Mon, 09 Jun 2025 23:12:33 GMT
SHELL [cmd /s /c]
# Mon, 09 Jun 2025 23:12:34 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 09 Jun 2025 23:12:35 GMT
USER ContainerAdministrator
# Mon, 09 Jun 2025 23:12:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 09 Jun 2025 23:12:39 GMT
USER ContainerUser
# Mon, 09 Jun 2025 23:12:40 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 23:12:48 GMT
COPY dir:2a5431c9629d8e59dc59f707822e3e4d9048b856e0212fd4224a68120121ffaf in C:\openjdk-25 
# Mon, 09 Jun 2025 23:12:55 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 09 Jun 2025 23:12:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1003373525a8ed0b15e1dca1e3aef012927d925db98b44021d76e6f23c3c746e`  
		Last Modified: Mon, 09 Jun 2025 23:13:37 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bf818ca3ea01ea15b23dc73d8bededec0cbdfc48be666b022dd0708cd8a822`  
		Last Modified: Mon, 09 Jun 2025 23:13:37 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8519cf712e1ca6744d0bfc70f6093da6fd219a97d79dc84cad01de4b10bea5b6`  
		Last Modified: Mon, 09 Jun 2025 23:13:37 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6093fe074dd87066c829ddcd18e1c94b472c3f0d0a4218f0021ee244275f3bf`  
		Last Modified: Mon, 09 Jun 2025 23:13:37 GMT  
		Size: 76.4 KB (76441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1933298b2b5a6e24ae6a6150e4508bc7ac35e2e45532e7d7b151e8276908c2a5`  
		Last Modified: Mon, 09 Jun 2025 23:13:37 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062354e9a47614b9052df304423bd42d6da55c914bc6545d03a8af984bcb160a`  
		Last Modified: Mon, 09 Jun 2025 23:13:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77269d2076464ffbc58d7c07260f3f0fe6be3ad65b5858b73c93df9884d37693`  
		Last Modified: Tue, 10 Jun 2025 00:24:36 GMT  
		Size: 218.4 MB (218444457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8332fb289865e9e250f0b6806f29866f4f3659f0b9642ef41a86c90e521b9cff`  
		Last Modified: Mon, 09 Jun 2025 23:13:38 GMT  
		Size: 114.6 KB (114555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb59fc796eb81898a42d36e09944a297b99b1464f967cdbd1a52656f5fce760`  
		Last Modified: Mon, 09 Jun 2025 23:13:38 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
