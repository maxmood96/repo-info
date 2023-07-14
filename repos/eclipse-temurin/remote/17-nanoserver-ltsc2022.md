## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9f946f682873a0eff34613f905a51c4a949ffe8516a65f14be0e70673ad2ec12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.1850; amd64

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
