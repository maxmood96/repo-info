## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:26e61e783b33c56b92405009b6d90d996786132bcfb7a92d838352345fb814d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1850; amd64

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
