## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b34c85f286da47fde1ccd5c9d8ba8e6905fd142a9b1ed36f4451b3e0d4e4195a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:2acf0f94ea9fba0a63b588cb73bb689e5a10c88b9f9a14249a16dee175b499c0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313191288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dda92616895f83aa681fe0e070f229bccd4f982ea23ed4d3469c4278ad7459`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 21:00:40 GMT
RUN Apply image 10.0.20348.1850
# Thu, 13 Jul 2023 22:10:51 GMT
SHELL [cmd /s /c]
# Thu, 13 Jul 2023 22:12:08 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 13 Jul 2023 22:12:09 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 13 Jul 2023 22:12:09 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 22:12:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Jul 2023 22:12:20 GMT
USER ContainerUser
# Thu, 13 Jul 2023 22:12:33 GMT
COPY dir:aa85dc89894032bdcf98e5da06633e8de4813537c791ddbe3fc8bdfa8596f8de in C:\openjdk-11 
# Thu, 13 Jul 2023 22:12:47 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Jul 2023 22:12:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc0a26bd90fcc4d863317c36d7ffec77a0a82a905697204d4dcbc76ec13b3920`  
		Last Modified: Tue, 11 Jul 2023 20:10:45 GMT  
		Size: 120.1 MB (120056465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb11750b624a775aa3c21a13406dfc54458855b8684e21efba5bbb9b27ee0b12`  
		Last Modified: Thu, 13 Jul 2023 22:28:35 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89984660d577657926e73c66b7fcde177c4950f5025a6bf33df1b51c7941e373`  
		Last Modified: Thu, 13 Jul 2023 22:29:15 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358706f4b9d417c390fd1a356f6730ec6de76a5302e7c2f57398692c1b10d8d5`  
		Last Modified: Thu, 13 Jul 2023 22:29:14 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54056a08569abd48b6a54847eaac67709826a7ca7acae552af5b59bf4af84f8a`  
		Last Modified: Thu, 13 Jul 2023 22:29:15 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d968b25a111ee3ef2e094c8629b039007c792fa75dc90fb9dc8ee726e9bd6c72`  
		Last Modified: Thu, 13 Jul 2023 22:29:13 GMT  
		Size: 85.4 KB (85378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe704e1ea918f25c3870438597179e08d0a4464642ae09ba8e7d80dd98dfd2e`  
		Last Modified: Thu, 13 Jul 2023 22:29:13 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01178de7f214a9aa0811193cf117330e6a8d67c5d249d871253e3377e8eae104`  
		Last Modified: Thu, 13 Jul 2023 22:29:33 GMT  
		Size: 193.0 MB (192983863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09752d02dca5c17d4f16b31185e02821dbbffb487b31f09131d5930034b58da5`  
		Last Modified: Thu, 13 Jul 2023 22:29:13 GMT  
		Size: 58.6 KB (58576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f05ea1917ecc22df9a5aa16f6de76594544f74c2e227cfe3be96b07f6837f66`  
		Last Modified: Thu, 13 Jul 2023 22:29:13 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:1ef98db3e4046746f74d1a6735dc5db36944cb859e9f4e123a89a9ea76cb1a1b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297546910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6565f7afaf0f966012cf5c752aabe21661bb897bd0ffaf85700dd267e4db31`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 21:36:32 GMT
SHELL [cmd /s /c]
# Thu, 13 Jul 2023 21:45:56 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 13 Jul 2023 21:45:56 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 13 Jul 2023 21:45:57 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 21:46:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Jul 2023 21:46:10 GMT
USER ContainerUser
# Thu, 13 Jul 2023 21:46:26 GMT
COPY dir:aa85dc89894032bdcf98e5da06633e8de4813537c791ddbe3fc8bdfa8596f8de in C:\openjdk-11 
# Thu, 13 Jul 2023 21:46:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Jul 2023 21:46:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13c473988daf5951866dd9b290bd6417227c1d7df6e811cfe11438d033a1eba`  
		Last Modified: Thu, 13 Jul 2023 22:19:06 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5e846269564d0de3e517f744d5343c3af6aab0a0d215cbae4dfd7844682853`  
		Last Modified: Thu, 13 Jul 2023 22:21:36 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381a5c657935102f755b0eab2f471dd57673d58ecfb70713a66b54375ce84b47`  
		Last Modified: Thu, 13 Jul 2023 22:21:36 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d43d6b7155e6d23aaa1f6c72dfb71758637584c1f720ac99c5dc3d845a1eb9`  
		Last Modified: Thu, 13 Jul 2023 22:21:36 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6baa4de76dd5a19dc307f4d2e4b2324b4cd1455e0977666b07c140c2031425c4`  
		Last Modified: Thu, 13 Jul 2023 22:21:34 GMT  
		Size: 74.2 KB (74167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedac62f2f7579a4d94d958738cdf7ff61a5554bd9fa8115458f10517eeccc5d`  
		Last Modified: Thu, 13 Jul 2023 22:21:34 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d152a5c6d7c135a2b83c506622781d7f0850ff22e1f017b022d4f4679a87c8`  
		Last Modified: Thu, 13 Jul 2023 22:21:53 GMT  
		Size: 193.0 MB (192972353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d18d9177d4ef4a84ea88c93b14cf5831fd0bd2457ff9144582ae0ffdd0456a3`  
		Last Modified: Thu, 13 Jul 2023 22:21:34 GMT  
		Size: 85.8 KB (85776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a748450915398778666ab0de8b0360e7d95e4e37c9e7d5c8db642645e56d957`  
		Last Modified: Thu, 13 Jul 2023 22:21:34 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
