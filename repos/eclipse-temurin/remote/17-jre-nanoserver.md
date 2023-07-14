## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:81eb2c86d42fc1bf0e170a561cf07a2c1f27fe8146940684e3e820bcb5e3022e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:1dccdc36359cea7741fa4e7709e0621c4cede5fb200a197f490ed4deb20cceda
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163536613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08dccc147e8b62cb4f2ee319b7f846c97f5238d893e6df8922c9b500dda52ff9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 21:00:40 GMT
RUN Apply image 10.0.20348.1850
# Thu, 13 Jul 2023 22:10:51 GMT
SHELL [cmd /s /c]
# Thu, 13 Jul 2023 22:13:29 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Thu, 13 Jul 2023 22:13:30 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 13 Jul 2023 22:13:31 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 22:13:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Jul 2023 22:13:44 GMT
USER ContainerUser
# Thu, 13 Jul 2023 22:14:30 GMT
COPY dir:8912d07424b5206284ef3b7586d69c3f366b527bba3d6f334194ae58c2152641 in C:\openjdk-17 
# Thu, 13 Jul 2023 22:14:41 GMT
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
	-	`sha256:fc3bb7d3b08585e7006db10d0efb38d0d5097d13a9c03d6f6bb609f4b6723685`  
		Last Modified: Thu, 13 Jul 2023 22:30:05 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bdafa75cc5580f6b0fa49c3884a62aa8ba03094cc553d547b9e00f9900c207`  
		Last Modified: Thu, 13 Jul 2023 22:30:06 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a747f9c3c773158031ce9d76fed5ee70875ad31e962c33ee5238ec428ee9e2d0`  
		Last Modified: Thu, 13 Jul 2023 22:30:05 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a356dac055f7c2cf9a35fb3d2b8dc149b6e7467794910a40a131f9ca4694fc`  
		Last Modified: Thu, 13 Jul 2023 22:30:03 GMT  
		Size: 85.4 KB (85361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6b987935162cb2642a417654de29c6fef695e46e6f29ebcac923ceb42e629b`  
		Last Modified: Thu, 13 Jul 2023 22:30:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dcb4bce0bdef05aeb1f7b7af331dd4ad1a726c5ca2497dc115b29924cd4a83`  
		Last Modified: Thu, 13 Jul 2023 22:30:41 GMT  
		Size: 43.3 MB (43326901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9137dfaa70645f7ec434e1ab72d60ff88f7fef878fb42f939ed648b002e95f38`  
		Last Modified: Thu, 13 Jul 2023 22:30:33 GMT  
		Size: 62.1 KB (62054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:182cafc16f5bd0ce851eb06914e1a90f6b9cd35da2f0f5bd6ff309745ae56495
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150847251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e47e6af4fee1155c1e3013e25d02c30854514b0067e3897b4b6293c79837ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 21:36:32 GMT
SHELL [cmd /s /c]
# Thu, 13 Jul 2023 21:56:06 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Thu, 13 Jul 2023 21:56:07 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 13 Jul 2023 21:56:07 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 21:56:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Jul 2023 21:56:17 GMT
USER ContainerUser
# Thu, 13 Jul 2023 22:00:57 GMT
COPY dir:8912d07424b5206284ef3b7586d69c3f366b527bba3d6f334194ae58c2152641 in C:\openjdk-17 
# Thu, 13 Jul 2023 22:01:09 GMT
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
	-	`sha256:a05f6ac66c39db0d9cf766b40ab551d1eb1a6c11ba37a7d7f748556244cf72a5`  
		Last Modified: Thu, 13 Jul 2023 22:24:18 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e9326b6aaa827e4805dd2487868100ccdfcd905a01354501ba1801c80080`  
		Last Modified: Thu, 13 Jul 2023 22:24:17 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d651bee386ed489c9f80ff819cc63f8dc41a52ccf08e9cca86e10395c3c87600`  
		Last Modified: Thu, 13 Jul 2023 22:24:17 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00eb69e43599c89adbbc7837cfc400349c6a432903f2d5e455ae5429a1a50cee`  
		Last Modified: Thu, 13 Jul 2023 22:24:15 GMT  
		Size: 67.8 KB (67754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3b7108ee6bf5772fd55ae58d7e27b8a3fbd4105ed184331e60895a6ec77459`  
		Last Modified: Thu, 13 Jul 2023 22:24:15 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ad3e50a95268289b7029c6d1011831745423d03b18787937bb60a3e1296797`  
		Last Modified: Thu, 13 Jul 2023 22:25:32 GMT  
		Size: 43.3 MB (43326947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2673722d7e7440f533564f9794c603a6c44e69d8fcd62d261027c6038a007b`  
		Last Modified: Thu, 13 Jul 2023 22:25:24 GMT  
		Size: 3.0 MB (3038509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
