## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:5b9cf22e56b8e63f572670f794157ff81615678449ba5130e09f542d65226140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

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
