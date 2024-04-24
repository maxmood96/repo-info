## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:2a1625db31fd50bc00c0f7d1a62f3a3dd49ce62494cf193975d70816134c465d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:472eaabca451f40e11e154954a35e363e0aa7763f80f436d40b90866ac2f05c7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222851433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59645ed51412bffc91dff8d24bda4d4cc7ad4d67a41a416da91e5b3aa3da62f8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:22:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 24 Apr 2024 19:22:38 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 24 Apr 2024 19:22:39 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:22:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:22:55 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:23:06 GMT
COPY dir:5498972beafb1de3e4749bc87b064f8ce9cec472aae9e7d0f4643a99f48638da in C:\openjdk-8 
# Wed, 24 Apr 2024 19:23:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a568162a8db2139c9b7f50bdca7e6de2f6e46f3a23196ccf7b33d019ad6c3f4`  
		Last Modified: Wed, 24 Apr 2024 19:46:08 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76150342796de52322a78b1675aa420817cbf16aa69b853f3213c97193064da1`  
		Last Modified: Wed, 24 Apr 2024 19:46:08 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d61c15b18ab0fae7ccb0fec0d9464105deb40fe2b2e29d96c6d93975524297`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792f549969d948ee4d8765477e3d71b4a2d4fa9c0c89daec775697ad31d12ad0`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 86.3 KB (86274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c5d1ba740a169c8c5fabb77a7268e210555e1c13d639548d947228a4f7d950`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f7f65d1806775b9c8297585522ec3b7b170e05b4b3be6937d2db568803d73a`  
		Last Modified: Wed, 24 Apr 2024 19:46:17 GMT  
		Size: 101.7 MB (101705268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb7440a247a985251799b5315f62efd778bab9d5492f8b0b99e9eed88dbc7e5`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 61.0 KB (60973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:43de2be4b109ce916e5817d2fbf91cd238a815fdce4d10aeac69f4a082ddf9d0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206734788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c412e835cff49c5148547874b6c60066201ab89a9b551f3bad16873108660b9b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 18:30:04 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 24 Apr 2024 18:30:05 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 24 Apr 2024 18:30:06 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 18:30:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 18:30:26 GMT
USER ContainerUser
# Wed, 24 Apr 2024 18:30:45 GMT
COPY dir:5498972beafb1de3e4749bc87b064f8ce9cec472aae9e7d0f4643a99f48638da in C:\openjdk-8 
# Wed, 24 Apr 2024 18:31:02 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1aba89d9ebacd4f1369cd48d26d09c1a19c37a1bb267bca108af48fc1aab5a`  
		Last Modified: Wed, 24 Apr 2024 19:33:30 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66a02d1909bba7585a63ed513f0c7c5bbd6364e3a52b3b363b25890a8bfa166`  
		Last Modified: Wed, 24 Apr 2024 19:33:30 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e870db953193353980429b04bed7cc708680f15d0c432e2aa6f6dda4ea88157`  
		Last Modified: Wed, 24 Apr 2024 19:33:28 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd079869a94c991c70a1182afbad7cc1fc3ab25e82ead25390f279108d4344cc`  
		Last Modified: Wed, 24 Apr 2024 19:33:28 GMT  
		Size: 65.8 KB (65774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ef74b03f97dccf54dafc9c09e7fef7c0f6b60eb15ed9450d9f147aaa750ae0`  
		Last Modified: Wed, 24 Apr 2024 19:33:28 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f9e4b9e4d95967e3af1dcf04dc7d6fc8b6bbc204b86880778ea4628a5cb80b`  
		Last Modified: Wed, 24 Apr 2024 19:33:39 GMT  
		Size: 101.7 MB (101696590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74d54a754bd7ea1bf423a7014a15e223b6ae396fabb5c8f8ce5700ece5baf95`  
		Last Modified: Wed, 24 Apr 2024 19:33:28 GMT  
		Size: 77.5 KB (77484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
