## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1f5e21dbe9c3bc853df9a60d794d965b461cfed1f265a0f3196f62f22383e757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:8ed95605eedf9ed9487578d73891a47e71f00857e26108e58dfb63b8e1b0df82
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305749277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50e88c7a2ff9c30d3c0ea3fbbad9cea07fc0db21a43e25e90b69b7a46a03bb1`
-	Default Command: `["jshell"]`
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
# Thu, 13 Jul 2023 22:13:57 GMT
COPY dir:124ac1113930ce4049263b0be6b87edbaf53b403e9545bc9faa31b4eed61cbf5 in C:\openjdk-17 
# Thu, 13 Jul 2023 22:14:11 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Jul 2023 22:14:12 GMT
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
	-	`sha256:9fc561de96d6bbac958f642172d022fe28a0367183044032623b5d1dfc3b3f98`  
		Last Modified: Thu, 13 Jul 2023 22:30:21 GMT  
		Size: 185.5 MB (185538344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a500b203b5aae206c7b55f169f0672b8314e521196c65e5f74df3d78cef835`  
		Last Modified: Thu, 13 Jul 2023 22:30:03 GMT  
		Size: 62.1 KB (62100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b17f5ed0367c5ba04b81145faa26ec738ea33325b9490e3c2a3e8786d4ad085`  
		Last Modified: Thu, 13 Jul 2023 22:30:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:c09c497bbbd99ad98f17c3d9f02f3d605de114a0b812e52307b523305afd9227
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293688044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bbff548e12aa7a6d85d177ba8a17fc509f4aea30228f299c5e09ed801e32c9`
-	Default Command: `["jshell"]`
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
# Thu, 13 Jul 2023 21:56:30 GMT
COPY dir:124ac1113930ce4049263b0be6b87edbaf53b403e9545bc9faa31b4eed61cbf5 in C:\openjdk-17 
# Thu, 13 Jul 2023 21:56:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Jul 2023 21:56:45 GMT
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
	-	`sha256:2d1c7c846a06ed5c7229fd063c6913899ce53f6300f8e38e8faa1401b3ee0d94`  
		Last Modified: Thu, 13 Jul 2023 22:24:34 GMT  
		Size: 185.5 MB (185537658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5110974d46f5d2f1bbe1b9f4a0b57ab814e76385e0b021fb44619f42f9ed1cc`  
		Last Modified: Thu, 13 Jul 2023 22:24:17 GMT  
		Size: 3.7 MB (3667459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f282e71d8cfad91cdd9fa9ffe1114a31419b1f5233c3780a698a853c0c7f199`  
		Last Modified: Thu, 13 Jul 2023 22:24:16 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
