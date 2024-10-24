## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:deb6071e82ff73e0d07b4c40d0f64656dba76332acb89c3dcea585a59b39ef76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:6fc41e066a95d825f79f29215942eb04a9ddf786d21d1b858d42503aebfea525
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.1 MB (347073479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4f0e5a7081ee58b69afd81c1bb8e0eb321a232f9010555c43a15a92e3c03f9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 24 Oct 2024 01:52:54 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 24 Oct 2024 01:52:56 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 24 Oct 2024 01:52:57 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:14 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:22 GMT
COPY dir:52d780064906626480ed3e0e10c20681fda9fbf2926de2858bcee46524c2c3aa in C:\openjdk-17 
# Thu, 24 Oct 2024 01:53:27 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 24 Oct 2024 01:53:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e14a5e51818e808f485b63a8c5b59c95f94a90e32bce1085f7ee31204e2f5f`  
		Last Modified: Thu, 24 Oct 2024 01:53:32 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2b291f8c50bd9084d4ef346c02ba8b5e5759eb1048bbb2cf75565c04308136`  
		Last Modified: Thu, 24 Oct 2024 01:53:31 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a0ae603ffad5e7a9dbe59b63290bd3dbb5ace3ebc34b792c6fb294c78e923b`  
		Last Modified: Thu, 24 Oct 2024 01:53:31 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea8eef632fb2f80e35087dd21f4b98034962f2cb1dd774f82c74f7884fe5056`  
		Last Modified: Thu, 24 Oct 2024 01:53:31 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d96842af7a7eefba20691d4a785266ac74807824c747dfa62b008187c66c8e`  
		Last Modified: Thu, 24 Oct 2024 01:53:30 GMT  
		Size: 66.1 KB (66123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892ad033844a48ee3ea5ea6139185bb9b678e25453e86d79e386d9e55128f717`  
		Last Modified: Thu, 24 Oct 2024 01:53:30 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1ef675b20c0bc838ae3cb9e0806680d90271961b195de5307d70d91dec91cc`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 188.3 MB (188302008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44cce250024bc6049c0181932235a1cd202b8f71dc58acb7e3757b50ee37d83`  
		Last Modified: Thu, 24 Oct 2024 01:53:31 GMT  
		Size: 3.6 MB (3605410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f79af487f2f308fe78df691f443a1d19c02d1e0b1381e5894ac9162dde1b737`  
		Last Modified: Thu, 24 Oct 2024 01:53:30 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
