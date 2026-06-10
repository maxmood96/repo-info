## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1bf50f4a1f99d39d89c82d8e6ec32e37682a3e226e3cb8fa5a0dea3a36d0e819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

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
