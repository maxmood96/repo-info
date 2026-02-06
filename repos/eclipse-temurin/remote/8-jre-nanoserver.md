## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4c163d7578af8b6b839ac7b7d622053d4e7dda6aff89a3378e7c97963ac22fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:d2ca7db8c72efedffe14d16c27ce29082f5e3efb08d7f1fe297f064b4ff7b76f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239205902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c598c2c0b7629d1b58e07e7bcc6346c3041b7147e30ff2058141db983efece87`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:39:33 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:33 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:39:34 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 05 Feb 2026 22:39:34 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:39:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:39:41 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:39:51 GMT
COPY dir:e192ec1627bb02acae941746a6647cea6857b84f7daa4f746913822a0bac9dcc in C:\openjdk-8 
# Thu, 05 Feb 2026 22:39:54 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df349792790c4603c9504247c1449180418599d0164b33b93a0b3aa9a3e9311`  
		Last Modified: Thu, 05 Feb 2026 22:39:59 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0e83fb2de8962a9126aa8e8d5b8e12cb311dea4c731ee36f1430ecaaef4d1d`  
		Last Modified: Thu, 05 Feb 2026 22:39:59 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd473797effe0a43be509bc3cf5e71b1090b140f4480f00ca643671aaae700`  
		Last Modified: Thu, 05 Feb 2026 22:39:59 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec20a111b7a98979b598122227d70b9b2c120e91675d6e444d260e77e1ffc19`  
		Last Modified: Thu, 05 Feb 2026 22:39:57 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552b51066b759b6e9c2c6d7afeffefa924131798b9f476ab7c13e0e6412963fb`  
		Last Modified: Thu, 05 Feb 2026 22:39:58 GMT  
		Size: 70.3 KB (70349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2804d9544513389fbf9eddaff58af66a6e8be19d43a3956fef198d08c8d2da45`  
		Last Modified: Thu, 05 Feb 2026 22:39:58 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a0a5928b273b55b2e4fb33d3e0339fa432174d3e1a175013ae6ec02d9f4efb`  
		Last Modified: Thu, 05 Feb 2026 22:40:02 GMT  
		Size: 40.0 MB (39969939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fc1496c82cc053b6c965c0be8b97eb7dcee62a6ea373a066d99fe71dafe465`  
		Last Modified: Thu, 05 Feb 2026 22:39:58 GMT  
		Size: 83.7 KB (83662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:8f899cb54b4e1c797e151ee69eb9e01dec21f6892b742f9740d7b2673964d49b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166855375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e553eeb2f291e788cd0516fba67169c23b32e3388ba3fa2d0fc0c2a9e3c6e5b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Thu, 05 Feb 2026 22:39:10 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:10 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:39:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 05 Feb 2026 22:39:11 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:39:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:39:17 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:39:27 GMT
COPY dir:e192ec1627bb02acae941746a6647cea6857b84f7daa4f746913822a0bac9dcc in C:\openjdk-8 
# Thu, 05 Feb 2026 22:39:31 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23de278b82f92ecbfac0e648c5cf22813568a8f13d4ba4bd5ec7fc52ce663b7c`  
		Last Modified: Thu, 05 Feb 2026 22:39:37 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f3dc02e8be4cd0bd13d074fc5f93ec7fb879abf9400aea2f7bd595b32db2ad`  
		Last Modified: Thu, 05 Feb 2026 22:39:37 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98acc16d873a3d57f618d38677d4e2fc816864c09772107c119623b2ac5654e3`  
		Last Modified: Thu, 05 Feb 2026 22:39:37 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8febc22fec971d8b61a85f3bbfaaeaf7c7d719622a7feae440a0049085a04ccd`  
		Last Modified: Thu, 05 Feb 2026 22:39:35 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee3f75af7611e366ca8272103452ba099c252f48aa7f5809fd0faea597cf093`  
		Last Modified: Thu, 05 Feb 2026 22:39:35 GMT  
		Size: 73.0 KB (72998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed63846e05dfb3b5f56c5137cacde4f2326f29deefd96b50009383ae671881`  
		Last Modified: Thu, 05 Feb 2026 22:39:35 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d3a26b89d6dc84fc8e041d6cc93faa9f91926ff9f01f30e42ba349b0abe5a2`  
		Last Modified: Thu, 05 Feb 2026 22:39:40 GMT  
		Size: 40.0 MB (39969605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30157b7531a8473645b095907385f9bbbb2c753f6c8be83fa74a55eabf3af71`  
		Last Modified: Thu, 05 Feb 2026 22:39:35 GMT  
		Size: 110.6 KB (110584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
