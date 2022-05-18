## `openjdk:19-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:2fe9eb4214fcdd213417e87e60a428029a8806e9687557b453be7024929941bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `openjdk:19-jdk-nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull openjdk@sha256:ba2e74b309ba2947559ea11f96b6f81f163f3d6ff004e8c5848a161a881e04ec
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297511795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1738b7ad9815cabd37916c1c6e37d3951f9a39d1beeea02b19ca3d03acbb7369`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:49:49 GMT
SHELL [cmd /s /c]
# Wed, 11 May 2022 15:33:35 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 11 May 2022 15:33:36 GMT
USER ContainerAdministrator
# Wed, 11 May 2022 15:33:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 May 2022 15:33:48 GMT
USER ContainerUser
# Wed, 18 May 2022 01:17:19 GMT
ENV JAVA_VERSION=19-ea+22
# Wed, 18 May 2022 01:17:33 GMT
COPY dir:08689c564cf080d4cc8c0778081f9ef82d299b76adb424cd32c65db657a1395f in C:\openjdk-19 
# Wed, 18 May 2022 01:17:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 18 May 2022 01:17:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5592374182790eb41396d922d16be86f39a125562f29ea3ed221a94aeec2af45`  
		Last Modified: Wed, 11 May 2022 16:00:35 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27258317e27e0cfabcf779836e0e38e0809f5ba5b2e2ce61b0c4761494eabf2f`  
		Last Modified: Wed, 11 May 2022 16:00:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90f575ce9dbc595a6266a2d907de169473af97a71414d6a81d122bfc9cd5e39`  
		Last Modified: Wed, 11 May 2022 16:00:33 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40175500d750084c8212d8ea8f70d757ec3255fcb2fe588e2663c8a405187094`  
		Last Modified: Wed, 11 May 2022 16:00:33 GMT  
		Size: 74.5 KB (74495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d665e0106401630d154ad3a944dc128966740b1e1b21d2fbeab345b8da177a`  
		Last Modified: Wed, 11 May 2022 16:00:31 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00cff59c10e61481491feafeed4534bc3a61d1eb45edcaab574e65a397fc67b`  
		Last Modified: Wed, 18 May 2022 01:29:18 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591b6d97b20661fb8b7821477e286cb765edef0db1909471b6ca122cc78738b4`  
		Last Modified: Wed, 18 May 2022 01:29:36 GMT  
		Size: 190.7 MB (190652099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c154fc3129f00791aefc3a8aa3d0d9b274e40cadc79a280502151dd65310f5e`  
		Last Modified: Wed, 18 May 2022 01:29:18 GMT  
		Size: 3.6 MB (3644445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a806047f1c110692edcc4856cd9303e4731e9935b051b20ab961f7acdd750b75`  
		Last Modified: Wed, 18 May 2022 01:29:18 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
