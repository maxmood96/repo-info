## `openjdk:26-rc-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:340cf5e8cb9463131736ec35f816761720ddbd097ce35e006fafda594e062876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `openjdk:26-rc-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:853dad11791669eea995b8966d5f688079171d1025a30bf9d45579bdb53a5955
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.4 MB (423374163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f88542fae91124ef62cd4d9ad49b4293199724f313ae709ac9f6427b04b3f03`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 17 Feb 2026 20:05:36 GMT
SHELL [cmd /s /c]
# Tue, 17 Feb 2026 20:05:37 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 17 Feb 2026 20:05:37 GMT
USER ContainerAdministrator
# Tue, 17 Feb 2026 20:05:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 17 Feb 2026 20:05:47 GMT
USER ContainerUser
# Tue, 17 Feb 2026 20:05:48 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 20:06:15 GMT
COPY dir:48d9a1614aae77abafeeb59360dca42b580c313456033330908c8e794bbb7778 in C:\openjdk-26 
# Tue, 17 Feb 2026 20:06:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 17 Feb 2026 20:06:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf80968c83e83bc1a25677379f75f42a5bd3f0052a93e3737038836e80bb3cb4`  
		Last Modified: Tue, 17 Feb 2026 20:06:26 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2d755a02907768e1d77008be1cd86fa5db9657747f6cccd54c17e654377292`  
		Last Modified: Tue, 17 Feb 2026 20:06:26 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c34f9a0966957346ad4222101b17df008d85f8d2433e2687b1794b0a8e9971`  
		Last Modified: Tue, 17 Feb 2026 20:06:26 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1534d3a2b3df4338689780482d39f9b6084f660a085d61bbfb5448c37a5cec`  
		Last Modified: Tue, 17 Feb 2026 20:06:26 GMT  
		Size: 70.4 KB (70428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695a1d423570b9f0ad822705e891d0439e6fb126b6b76f75a450123ef58380c4`  
		Last Modified: Tue, 17 Feb 2026 20:06:24 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d232983bd9c256974ce84a9f329f8bd6253c0f15d7c4917a5e5ca809da729ce5`  
		Last Modified: Tue, 17 Feb 2026 20:06:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5605ee12b02402d666576e82a13d60735ce4c97df6fef785d7d4fb9212718482`  
		Last Modified: Tue, 17 Feb 2026 20:06:39 GMT  
		Size: 224.0 MB (223950875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f78980537ae08246d6ad5d868b1da5a403d542723617d33d3b0a0802100ec1`  
		Last Modified: Tue, 17 Feb 2026 20:06:24 GMT  
		Size: 94.8 KB (94827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50822252cce3ed7ecae40ea6d407577652b0bea603edd58405ecf17d264d5f2`  
		Last Modified: Tue, 17 Feb 2026 20:06:24 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
