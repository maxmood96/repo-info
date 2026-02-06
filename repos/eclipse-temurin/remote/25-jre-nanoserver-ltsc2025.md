## `eclipse-temurin:25-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:5eeebe558e55aff9a2a3b39b549791ca01a451e0459cb4c1459ef361b0177858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:233f450dce484d6b2366f6cfc0fff63ca5809e21b0cd8ad44e9fa6727ec5f790
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257841999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73aa9698176a631a90902a31497021210c50815cb403e654b75be0de36d015b5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:39:51 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:51 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:39:52 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 05 Feb 2026 22:39:52 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:39:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:39:58 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:40:10 GMT
COPY dir:15db28d5461f0a5f42074eb42e42a8535b9576d6847f4e637cb0dcfe9abfaabd in C:\openjdk-25 
# Thu, 05 Feb 2026 22:40:15 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce85ca2bfb978cc5d94873d183d6db4b69408dd21ac23ad11dd4a35e0dc29fd4`  
		Last Modified: Thu, 05 Feb 2026 22:40:20 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988408154b3c39476b46d2f28f2b279bbb62753a97dd9e79c162d16e1107051`  
		Last Modified: Thu, 05 Feb 2026 22:40:20 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3c2c1c8c64bdf8074ac25bbf8be7ff38c94f8ecd1d9aba383826801c6c05be`  
		Last Modified: Thu, 05 Feb 2026 22:40:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f2e02b82a1c74d89595bbb5e70a7a78944099715443a6f249260ad7fe8e95`  
		Last Modified: Thu, 05 Feb 2026 22:40:19 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcc119ab64fc917a7efeb7fa2f7e0110438534e710fdbdf6c641020e1240c92`  
		Last Modified: Thu, 05 Feb 2026 22:40:19 GMT  
		Size: 74.0 KB (73976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db31d84ae7a0a83df2b3ea935d8a93098e027f58ff69ad849998a8b76108612d`  
		Last Modified: Thu, 05 Feb 2026 22:40:19 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fe26fd07d1cacdbd80bfe5e3dbbf5e4f454f4ed0cb798019181980177fe103`  
		Last Modified: Thu, 05 Feb 2026 22:40:27 GMT  
		Size: 58.6 MB (58583131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea66c3477d18218dde110a490c9b3342a452279d48f04fbb3708b95e1d98bcc8`  
		Last Modified: Thu, 05 Feb 2026 22:40:19 GMT  
		Size: 103.0 KB (102964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
