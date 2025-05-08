## `eclipse-temurin:8u452-b09-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:10d9728cb194e344838a966fd52e2f60d875a04c26060799631ff13d7ef16ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:8u452-b09-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:0c1538ce5b145cba9988690465cef23d4f82d5a9090faa373a62d2b4a2bb18d4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163279916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c88835e97a9bb1de307afb58f2fe5e1158007d68ec937822ff094161acb868`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Mon, 28 Apr 2025 21:00:13 GMT
SHELL [cmd /s /c]
# Mon, 28 Apr 2025 21:00:13 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 28 Apr 2025 21:00:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Mon, 28 Apr 2025 21:00:15 GMT
USER ContainerAdministrator
# Mon, 28 Apr 2025 21:00:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Mon, 28 Apr 2025 21:00:39 GMT
USER ContainerUser
# Mon, 28 Apr 2025 21:00:42 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Mon, 28 Apr 2025 21:00:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f64b6eb4a92f1246dad93a3c5b2ac90c54292500eaf3e947a262d79b15b524c`  
		Last Modified: Mon, 28 Apr 2025 21:00:50 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee035c8d011dfcede2d03d0c5081983419d614810ad1f8ce8ec1cd9e9b38ddd9`  
		Last Modified: Mon, 28 Apr 2025 21:00:50 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90abd3ce4e4cea7d993f8990b5740108428cfb7fb29db1260e7a700ef0ea9e5d`  
		Last Modified: Mon, 28 Apr 2025 21:00:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981d8c6d2c158fa1ef7e6b9749162e876026d117bcd4d92ab6942b4dd3f1204d`  
		Last Modified: Mon, 28 Apr 2025 21:00:49 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee12339e58527771d6d3bf7ee0ff454328e149028caad420b5c961e010ab4c6`  
		Last Modified: Mon, 28 Apr 2025 21:00:49 GMT  
		Size: 88.8 KB (88755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618da349be872c00c690a63682ccdb728d1872d2a330eecc880e044601737e25`  
		Last Modified: Mon, 28 Apr 2025 21:00:49 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0955a7f11aaf68d0f91af9d27f22baac006dfc8a1f174902984eef71b6b48501`  
		Last Modified: Mon, 28 Apr 2025 21:00:53 GMT  
		Size: 40.6 MB (40553112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffc1a7bd90288e4d032e6af82f0dd8d95fa0f51d118076988025c91644514be`  
		Last Modified: Mon, 28 Apr 2025 21:00:49 GMT  
		Size: 93.7 KB (93736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
