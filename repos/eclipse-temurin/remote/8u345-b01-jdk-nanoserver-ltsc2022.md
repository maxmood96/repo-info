## `eclipse-temurin:8u345-b01-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:550336936907dc31d2dafed157519cac5f8cf7bd92925eb0c45e4032ea949528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `eclipse-temurin:8u345-b01-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:371fe31c5ef746b614f2935b658cd2f9a1e827377ab41e86bb277e4a8ddf2955
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218834318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b5e627ec6e016c27c6ede4fc9ccdf685e8d354566b6c124e9376c2f60c4d87`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 15:54:21 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 15:54:21 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 12 Oct 2022 15:54:22 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Oct 2022 15:54:23 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 15:54:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Oct 2022 15:54:37 GMT
USER ContainerUser
# Wed, 12 Oct 2022 15:54:47 GMT
COPY dir:3f2d3aa63ba7a56176deaae1ba1b26dbdbe105074828954c77b0da527aacd6d7 in C:\openjdk-8 
# Wed, 12 Oct 2022 15:55:01 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:38fa349577729651ac1fc3ec785f908719a8100da5f5ba9bd3f549411061f583`  
		Size: 118.2 MB (118202895 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0ed0041e3584df1952980c3f73fd2b6e154328c7a0165f37dbe92ef94ae8a95`  
		Last Modified: Wed, 12 Oct 2022 16:12:53 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812a04e8585e8b3fa1625525f7078c3fe8bdc3552beb86abe3186aeaf9332b2d`  
		Last Modified: Wed, 12 Oct 2022 16:12:53 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ef3610b04a50a6280701b19afc7e8b37b0d80c7e83845179c546c7890b1914`  
		Last Modified: Wed, 12 Oct 2022 16:12:53 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56128496f65019ddc28a9cde56ac2a0be3562bafdd0b336e9ee10ff364876210`  
		Last Modified: Wed, 12 Oct 2022 16:12:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfc3a606e27a41483ff4916dccc96b24730ef6ad9dbc0a2deb76341e07a3745`  
		Last Modified: Wed, 12 Oct 2022 16:12:50 GMT  
		Size: 85.4 KB (85425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ad17f557c1d2566ec24fc1e66666d4f818ee093ff0b5275dd7b6a2256a3b94`  
		Last Modified: Wed, 12 Oct 2022 16:12:50 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7113a94ba56b27c358df5311cf0e51c67099ad6d44f6cd0e5e09eb5b0a0e30d`  
		Last Modified: Wed, 12 Oct 2022 16:13:02 GMT  
		Size: 100.5 MB (100478158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352cc42857a77b15c89b1df53c5dbab800b0d17173db5322cf5c92236adac011`  
		Last Modified: Wed, 12 Oct 2022 16:12:50 GMT  
		Size: 62.1 KB (62125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
