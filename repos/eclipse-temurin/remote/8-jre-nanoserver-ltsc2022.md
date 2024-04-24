## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:40974a91ea58531113e777e78a3d3b0d7d4260cf6715a4726864f37a2732238a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:fc14cbda97ce2efd60acf69433d62157766f726bd7c710fd29a34f156a2ac9ef
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394e9f94609f1b552ddd7569d0f9420b02b4d17619f016614192ed072947787b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:22:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 24 Apr 2024 19:22:38 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 24 Apr 2024 19:22:39 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:22:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:22:55 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:23:37 GMT
COPY dir:2b748c8b95a49802258ef446e3948354b660cf39e9ffa8b2cf36461ec042c5c0 in C:\openjdk-8 
# Wed, 24 Apr 2024 19:23:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:4a568162a8db2139c9b7f50bdca7e6de2f6e46f3a23196ccf7b33d019ad6c3f4`  
		Last Modified: Wed, 24 Apr 2024 19:46:08 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76150342796de52322a78b1675aa420817cbf16aa69b853f3213c97193064da1`  
		Last Modified: Wed, 24 Apr 2024 19:46:08 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d61c15b18ab0fae7ccb0fec0d9464105deb40fe2b2e29d96c6d93975524297`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792f549969d948ee4d8765477e3d71b4a2d4fa9c0c89daec775697ad31d12ad0`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 86.3 KB (86274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c5d1ba740a169c8c5fabb77a7268e210555e1c13d639548d947228a4f7d950`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a138370e43b7219d7ce691dec52305825c312df34e0e0ff0a470544a32997a`  
		Last Modified: Wed, 24 Apr 2024 19:46:34 GMT  
		Size: 40.1 MB (40117772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdb7f347f4c25ad39fabe032d57709fb516f38702f27580f71a5753a3609492`  
		Last Modified: Wed, 24 Apr 2024 19:46:28 GMT  
		Size: 61.0 KB (61012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
