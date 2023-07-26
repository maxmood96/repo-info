## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1006553bc15b4c1c803319cc1116073e76f0353d16c039766d98b5b695968dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:06a25a33d39e6c149f4a0a6d3b96759601b5c29cf25f0644c56273eecf880a6d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163421008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57e42a6d53d5542134af3be8f0c2472bafa6f0fa3ce79efa4f7ff811544831d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 21:00:40 GMT
RUN Apply image 10.0.20348.1850
# Thu, 13 Jul 2023 22:10:51 GMT
SHELL [cmd /s /c]
# Wed, 26 Jul 2023 00:27:24 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:27:25 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 26 Jul 2023 00:27:25 GMT
USER ContainerAdministrator
# Wed, 26 Jul 2023 00:27:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 26 Jul 2023 00:27:36 GMT
USER ContainerUser
# Wed, 26 Jul 2023 00:28:24 GMT
COPY dir:bb977dad5ac490fa947ae016040faee9a62c080b2232e87b0466ed93d95df9ed in C:\openjdk-11 
# Wed, 26 Jul 2023 00:28:35 GMT
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
	-	`sha256:6f6fc7da52cd85c46d7cc9f4b0fe25d75d7e3cfcaa2dfc65ebac000529276d57`  
		Last Modified: Wed, 26 Jul 2023 00:34:25 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835a4cdfb9b1958fb13255c78147171f9d8747a6fa5a2719e6bfc9da55fd9f88`  
		Last Modified: Wed, 26 Jul 2023 00:34:25 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46453ada3c9c1d0d1c66cf1fc4b47ec80b2e70a8efc7bc57d3032202abebf733`  
		Last Modified: Wed, 26 Jul 2023 00:34:25 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075d5243707d8e6924ce011650fd2ae3e47c22405846bcbf95e4307ed0f9da5e`  
		Last Modified: Wed, 26 Jul 2023 00:34:24 GMT  
		Size: 80.2 KB (80184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18907ca6b61aec2fab8b9c92eba73443a66ae1c03a167e26d6be34a7ba63020`  
		Last Modified: Wed, 26 Jul 2023 00:34:23 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0782a62fc04810401abec4f8cc0183be9f1dac6b5157381535f39064f411953`  
		Last Modified: Wed, 26 Jul 2023 00:35:02 GMT  
		Size: 43.2 MB (43217467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167435ad4c83f7d9f422a5fa51f82068d5f7588cdc913619a3c7cd3f9b136f19`  
		Last Modified: Wed, 26 Jul 2023 00:34:55 GMT  
		Size: 61.1 KB (61088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:272a50e75adefe2aeb477ab03ca6fa414909a9113b0e8390f78abb3f24d5e0be
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147760450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08dad3dce5ac50c191441c56d2365385efbf296a993c08824c2c0d609a75447c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 21:36:32 GMT
SHELL [cmd /s /c]
# Wed, 26 Jul 2023 00:20:55 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:20:55 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 26 Jul 2023 00:20:56 GMT
USER ContainerAdministrator
# Wed, 26 Jul 2023 00:21:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 26 Jul 2023 00:21:06 GMT
USER ContainerUser
# Wed, 26 Jul 2023 00:25:53 GMT
COPY dir:bb977dad5ac490fa947ae016040faee9a62c080b2232e87b0466ed93d95df9ed in C:\openjdk-11 
# Wed, 26 Jul 2023 00:26:03 GMT
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
	-	`sha256:8cf417bf3467803e12fc9a31b5e6497d2433421e1fb614aac2984cf758f5b24b`  
		Last Modified: Wed, 26 Jul 2023 00:32:45 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8192126e41b0371c9ae3c94a72cf1c2d3e7d560a0c53ceaa0b4909e58ec91515`  
		Last Modified: Wed, 26 Jul 2023 00:32:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77854ff76c4d4dfbd3606d0a022401e89a7022cb27b1f8bfcc6d01883b30c37`  
		Last Modified: Wed, 26 Jul 2023 00:32:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd03a2c299188954a07fc8e131eafc52f6b71166fc234d29f4ee37a48e0c882b`  
		Last Modified: Wed, 26 Jul 2023 00:32:43 GMT  
		Size: 71.3 KB (71337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4ec240d039cba153cd22b6d0835e907ed1b0f578b82283a6610e6a6144c91e`  
		Last Modified: Wed, 26 Jul 2023 00:32:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0dd67368193848898bd84504cddef9d4a631c238cb4a4c5642d0945557f74dc`  
		Last Modified: Wed, 26 Jul 2023 00:34:01 GMT  
		Size: 43.2 MB (43219894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4419be0847ee59d306a768dfdc6ba2171a5e1da24a9de7c95557b16085a2cff7`  
		Last Modified: Wed, 26 Jul 2023 00:33:54 GMT  
		Size: 55.2 KB (55210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
