## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:cd87f6ee4371635d66f7d1381a287c6d4e808e7c520e05f13b334b040727a4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:2056bd72b5cd7e6477d6651b736149a2f61c0f40996e780bb4ec2484d0cf7106
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163370388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bbc5eb45869234c39560efaf76f747c9f61cad92d344ec05ec924460b65b0e1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Thu, 13 Jul 2023 22:13:07 GMT
COPY dir:b6e5aca1f3f361bc79d6ed078f0846fae24cf0b7748963379a92b2a6511b98d8 in C:\openjdk-11 
# Thu, 13 Jul 2023 22:13:19 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:7ccbe1e205176af45d899f18aaf4c4a3bde87fb93a628a8ca1564c952ea1dbd0`  
		Last Modified: Thu, 13 Jul 2023 22:29:53 GMT  
		Size: 43.2 MB (43164106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd250776ef4eb8d0bff369786434e22b6de84e57179ad0ac1b3b861bd744f803`  
		Last Modified: Thu, 13 Jul 2023 22:29:45 GMT  
		Size: 58.6 KB (58593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:842652d09c37163e6e9362954612862789ae4ac2707fd494f7d2fcfd2122353c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147709324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a0273759b1e163a6ec94c657670fec8153f25e3cad0209a3b878e7fecfe189`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Thu, 13 Jul 2023 21:50:50 GMT
COPY dir:b6e5aca1f3f361bc79d6ed078f0846fae24cf0b7748963379a92b2a6511b98d8 in C:\openjdk-11 
# Thu, 13 Jul 2023 21:51:01 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:4e03b26676536624f7945babd94b518b5eba867aaadd2b6fb3a6899f7ca95203`  
		Last Modified: Thu, 13 Jul 2023 22:22:50 GMT  
		Size: 43.2 MB (43172726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a17d046706333e779595137f7e47374df116f82235634d02bfde1f234b942`  
		Last Modified: Thu, 13 Jul 2023 22:22:44 GMT  
		Size: 48.8 KB (48843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
