## `openjdk:8-jre-nanoserver`

```console
$ docker pull openjdk@sha256:146feb100646171fcf0d0f09abad69b5b6d816dca5f1a870e9392e5fc19240a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `openjdk:8-jre-nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull openjdk@sha256:4831dcdafb2d480a36ebf5a783bb9ef12df50f1851637068a67d52b425ad4c2e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141498662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbaba32df0009dcbe2bfc251f83088bc1f0d336708e9fcf45598f447f1fb3ca4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 15:16:11 GMT
SHELL [cmd /s /c]
# Wed, 13 Apr 2022 17:21:37 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Apr 2022 17:21:37 GMT
USER ContainerAdministrator
# Wed, 13 Apr 2022 17:21:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Apr 2022 17:21:44 GMT
USER ContainerUser
# Wed, 13 Apr 2022 17:21:44 GMT
ENV JAVA_VERSION=8u322
# Wed, 13 Apr 2022 17:24:17 GMT
COPY dir:f4c77e4259f68c5f890bc7ab442034fb0a5366735393f4c5400d26f276285797 in C:\openjdk-8 
# Wed, 13 Apr 2022 17:24:26 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ea4009814dceb50337c66614a6008cfc2fb73ce53e62162bce071ef6ea1adf2d`  
		Last Modified: Wed, 13 Apr 2022 15:58:06 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65fb95ee42514e5278fb1f68d4225d0a5bba71921defb635d841ca30789226f`  
		Last Modified: Tue, 19 Apr 2022 01:19:34 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b00dbd36f2154a4eabea44e9a5d88c98927e03b469bb16de373838d0f29d1e`  
		Last Modified: Tue, 19 Apr 2022 01:19:34 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c635236ace6c57e8af5a6a467722bb1484d5ae5aaf133d60a5475aef5f4d2c4`  
		Last Modified: Tue, 19 Apr 2022 01:19:32 GMT  
		Size: 72.2 KB (72156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9131ef298cbc9163210fbeb93d70aed6922673cebc88b8563ea8ea489357b1c`  
		Last Modified: Tue, 19 Apr 2022 01:19:32 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ed6c834b69ab81bc5dcc57cf62299abe031d36fb332b26b0e30ec3ae7055dc`  
		Last Modified: Tue, 19 Apr 2022 01:19:32 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed90466dea86fd7adfec615570b30dc5801e9de7997cf39169473eb3b3521f5f`  
		Last Modified: Tue, 19 Apr 2022 01:20:47 GMT  
		Size: 38.3 MB (38266210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0233ff156f132d7f7b9db995a7e5139bc05648d8da3e95d46368a70841c82052`  
		Last Modified: Tue, 19 Apr 2022 01:20:41 GMT  
		Size: 58.5 KB (58532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
