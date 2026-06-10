## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:55981e2a68818b7cb70895299d1f9f9edddb83ffe6927e55147f38dd2b29d38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:8b024af1942d6cf5a629b4670f3ba81232c3e0ebbf2c1ab4093c85d66688cb66
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.7 MB (240694077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18a0a5e3973eac421bb45cd0243908bf5013913354a085f41aaf14e698eb0f7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:21:04 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:21:06 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 09 Jun 2026 23:21:06 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 09 Jun 2026 23:21:07 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:21:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:21:14 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:21:40 GMT
COPY dir:2f70d7e82fbe25185baf6a6b1e05b870cb38c3ad05aac5b5932c695a93320f91 in C:\openjdk-17 
# Tue, 09 Jun 2026 23:21:46 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10fe762a1b6d4dbf9a5fa90d4f6c8d2f34644565ceae022d590912c5ad9b609e`  
		Last Modified: Tue, 09 Jun 2026 23:21:52 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bc410d1d6f8b0cd8f9417327a6ded7a86ef4e45767af7ccde90b61da61c5e9`  
		Last Modified: Tue, 09 Jun 2026 23:21:52 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5c2196ccfb3747b337a90e9dfb61ae955a1812c8ca39d1e98fadf5c8695df4`  
		Last Modified: Tue, 09 Jun 2026 23:21:52 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17a05d3d6983ae6fcb36c6bb95aa8280226812143c0e8eb45d88be76341432c`  
		Last Modified: Tue, 09 Jun 2026 23:21:50 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4471bed5bfe3e2643face05a91fe269eadc9fe51b8da0e46af5cb0daccda45ba`  
		Last Modified: Tue, 09 Jun 2026 23:21:50 GMT  
		Size: 76.9 KB (76906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a11bfd0ebca3c0d3ece7958ab1b1178fd9103dfd97bfb9952916d2cee658f0`  
		Last Modified: Tue, 09 Jun 2026 23:21:50 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee877f926189f072ba8af825c5ef33e1ce9436fb18a80480ab9361857ba8839`  
		Last Modified: Tue, 09 Jun 2026 23:21:57 GMT  
		Size: 43.8 MB (43834420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42078dc0a15b175108c2b692d61ea1b8ef1d6d625768a879a7523ba5bbe7c783`  
		Last Modified: Tue, 09 Jun 2026 23:21:51 GMT  
		Size: 109.5 KB (109498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:fde639754147272b76e191b49cabf35053728693174c3ba54784e3ca21101eab
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (168019051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83593a68c0d8dbff99a73e0d9151fd8aef4d3ede4b8635eeaa7d651ee97e826f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:21:56 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:21:56 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 09 Jun 2026 23:21:57 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 09 Jun 2026 23:21:57 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:21:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:22:00 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:22:16 GMT
COPY dir:2f70d7e82fbe25185baf6a6b1e05b870cb38c3ad05aac5b5932c695a93320f91 in C:\openjdk-17 
# Tue, 09 Jun 2026 23:22:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb5700dfb290eb9db754f3ee1692dfa9331c95cd3d0441290f84448e0ecfae`  
		Last Modified: Tue, 09 Jun 2026 23:22:26 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f34c46821c42c59518f12e4dbcd2b6b48333d7b57b78c7b49f6ee180459d7ce`  
		Last Modified: Tue, 09 Jun 2026 23:22:26 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bae0afaa5151cc61885816bf12907f1f0655fd410af95c8a9aee501cbbe2c6`  
		Last Modified: Tue, 09 Jun 2026 23:22:26 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f472cf45c8ecd9d3db1479e142a2e42561812239b0862da551ea5fab8918f663`  
		Last Modified: Tue, 09 Jun 2026 23:22:24 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42c0bad74420a6dc97ae401b4f3bc82c857c3a3ef7f134b16467a3fd59ec82e`  
		Last Modified: Tue, 09 Jun 2026 23:22:24 GMT  
		Size: 82.8 KB (82839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb6488719dca8ed66edabad38cd92e07f73bc4db07070d685b33f590beff79f`  
		Last Modified: Tue, 09 Jun 2026 23:22:24 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f480f35ce400c924c347b20bf53cc84daab3b6a683ac4e9d9ce3d8dd56d94c8d`  
		Last Modified: Tue, 09 Jun 2026 23:22:30 GMT  
		Size: 43.8 MB (43833986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1027b3a180c646eeead6648670641168c7974bd4d72c14ecfadaf0a17089ac2c`  
		Last Modified: Tue, 09 Jun 2026 23:22:24 GMT  
		Size: 99.4 KB (99419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
