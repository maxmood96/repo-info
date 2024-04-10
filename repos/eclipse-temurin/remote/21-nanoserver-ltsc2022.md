## `eclipse-temurin:21-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1f488e02d3c9fdddd633a375a02d28ecc6e678fe025ef2afe850f6940e003df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:21-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:23632016f4b787c286efdc13bafaca485fce717606608002404fd82df48e9316
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322282663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83334d0f02ac130ebcf4ebf138058998bf04ab920c86bc5f5313daa3f6e0be7d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:39:00 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 10 Apr 2024 00:39:00 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Apr 2024 00:39:01 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:39:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:39:12 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:39:28 GMT
COPY dir:ef01cec12ba2d7ca328dd166c68dc318e8666a1382b059655285e6e080af62b8 in C:\openjdk-21 
# Wed, 10 Apr 2024 00:39:42 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Apr 2024 00:39:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312eb5a78cfa6f13afd6c4776c5cfe493c689b5a6deb5cd39bf9ff9d00255a57`  
		Last Modified: Wed, 10 Apr 2024 01:02:29 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95df9bac0b145e33b324b9280ecbb66171abba5ddef38594eb47a4fc3a2ac33d`  
		Last Modified: Wed, 10 Apr 2024 01:02:28 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed5f44d83d3572628a0f0cb2769958a659b4a554f7357fe3b0c8547827358c6`  
		Last Modified: Wed, 10 Apr 2024 01:02:28 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7734f46f55d9928b5b440034a3c44fb06258d40177cc9daa3766c5c8e8bc857d`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 83.9 KB (83899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5311424d09268f0b171cd86abf78d08316783448ff1587a1f93b33d9e33a57`  
		Last Modified: Wed, 10 Apr 2024 01:02:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e7f609d9f6f7cbf99f089394cda550324fb2b0db22a7349f832f7c890d4bd0`  
		Last Modified: Wed, 10 Apr 2024 01:02:48 GMT  
		Size: 201.1 MB (201124514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddff6017ad781f5ce37450ba422f36707b67dee2e32436f9c00f59e3e3f74c36`  
		Last Modified: Wed, 10 Apr 2024 01:02:26 GMT  
		Size: 74.3 KB (74277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f5e21d13c5c1a1a38c358f379c32dbab0e5cd38d92c837941b28d97ec836ad`  
		Last Modified: Wed, 10 Apr 2024 01:02:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
