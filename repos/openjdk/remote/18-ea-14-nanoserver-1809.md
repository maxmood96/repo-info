## `openjdk:18-ea-14-nanoserver-1809`

```console
$ docker pull openjdk@sha256:2bb1475f40937b87fea842bda7d92b9196f95a10b0f5cde036fbbc3dafbe57a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `openjdk:18-ea-14-nanoserver-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull openjdk@sha256:3002429b61859339dc9fdd36a92549a7c29fa12d6186e2e17830b24d1bfc73f6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (288975718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0d6c712b8a3f4c291af68e0b67f92e69aa91040fa03323447d9715f34c11e2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Wed, 25 Aug 2021 16:34:07 GMT
SHELL [cmd /s /c]
# Wed, 25 Aug 2021 17:06:45 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 25 Aug 2021 17:06:46 GMT
USER ContainerAdministrator
# Wed, 25 Aug 2021 17:06:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 25 Aug 2021 17:06:55 GMT
USER ContainerUser
# Tue, 14 Sep 2021 01:29:12 GMT
ENV JAVA_VERSION=18-ea+14
# Tue, 14 Sep 2021 01:29:26 GMT
COPY dir:51ec0ce7b7c9e4769d7449904cf647c2d5b50d722590d244bc3895b10447fd31 in C:\openjdk-18 
# Tue, 14 Sep 2021 01:29:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 14 Sep 2021 01:29:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9191bd6656c8ea186f621f667fb09a30387fae304b3e7817fd7e8258c022d185`  
		Last Modified: Wed, 25 Aug 2021 23:21:14 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529f54617b19374dc6ae56b7cbadea820f6613c38ef8eb5b3780625f824e7f70`  
		Last Modified: Thu, 26 Aug 2021 00:39:57 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17928612bd587dae3533403ae499232eb58f410a5e0875cca4930241ef47caa3`  
		Last Modified: Thu, 26 Aug 2021 00:39:56 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b2868a6eab69d3ff3c1ab6e50f537ef7b5671cd3a888b7fa6fcc521e63759`  
		Last Modified: Thu, 26 Aug 2021 00:39:56 GMT  
		Size: 71.1 KB (71120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1f7631bcd8fcfd1b84d19c43b45e42f54be2bafdb008157e4d2e8d7a64430a`  
		Last Modified: Thu, 26 Aug 2021 00:39:53 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d500a8267589ca2d90fae48fed33898da3859863d8a9e4b7e04fc7720bde358b`  
		Last Modified: Tue, 14 Sep 2021 01:34:57 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fec0136e944aa859244aa99cc5e67bbf06c68f3f0bc247d8409999067c69f8c`  
		Last Modified: Tue, 14 Sep 2021 01:38:19 GMT  
		Size: 182.6 MB (182601408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dded2e86206456532246ed6ac18455fbfbe22e81c0b62ae27567fe77625dbc4`  
		Last Modified: Tue, 14 Sep 2021 01:35:00 GMT  
		Size: 3.6 MB (3555379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5df2a32980c3f6ec16548d8e270b266b63644423f36e61698d64cc6d8db01be`  
		Last Modified: Tue, 14 Sep 2021 01:34:57 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
