## `openjdk:16-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:1c99b15fdbd62e8a535e261dc88b7d828580862c114852b6bc6f2ab759596734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `openjdk:16-jdk-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull openjdk@sha256:d345c4ec4b185904c925c9c3e377d051e3cff6e0a2e25e062a7883e3f8117f80
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285109494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f150c86b0dfa3aacea3f87b46d353e68eb107fbf6250465ce5726bd3839088b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 18:58:23 GMT
SHELL [cmd /s /c]
# Wed, 09 Dec 2020 18:58:23 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 09 Dec 2020 18:58:24 GMT
USER ContainerAdministrator
# Wed, 09 Dec 2020 18:58:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 09 Dec 2020 18:58:40 GMT
USER ContainerUser
# Fri, 08 Jan 2021 19:25:46 GMT
ENV JAVA_VERSION=16-ea+31
# Fri, 08 Jan 2021 19:26:24 GMT
COPY dir:fe6fd9f7c603fa326749cdfccbcd31289565cc3ddebf09394bdb282528bbec2c in C:\openjdk-16 
# Fri, 08 Jan 2021 19:26:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 08 Jan 2021 19:26:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fe9a51a0164bd1c063cbda08c4e22dc4f5d04a8047a3951d7441f37fb93c57f2`  
		Last Modified: Wed, 09 Dec 2020 19:34:04 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8993beeae33a05d68775319a4b9f9df44ac08ccfc62cb15113a36b06ad62d1f`  
		Last Modified: Wed, 09 Dec 2020 19:34:02 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340da9582f81cba4147b5da6d500dacd9f3ffdd520c3211dfb20153cd4ae71fc`  
		Last Modified: Wed, 09 Dec 2020 19:34:02 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f848f35781549a8c193011c95049cd95311b558af39d0f8057a5b460a459488`  
		Last Modified: Wed, 09 Dec 2020 19:34:02 GMT  
		Size: 64.6 KB (64579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636f94045101715dca150f5013879c45929dec9e849eac5b53631727e42bb8a6`  
		Last Modified: Wed, 09 Dec 2020 19:33:59 GMT  
		Size: 873.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e0ebf2fd91019dcacd0e39a4e6436e5370301e635a1b749e900f3ccc85b7f9`  
		Last Modified: Fri, 08 Jan 2021 19:36:58 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a8d4170d55c985ad2456734f0e63183fdb166d6208dce6e762ec3c8814b6a`  
		Last Modified: Fri, 08 Jan 2021 19:37:16 GMT  
		Size: 180.1 MB (180100262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf24ca02a6635df0916c0dcafe0855fa93c4dee804a68db5b2b974833261e4`  
		Last Modified: Fri, 08 Jan 2021 19:36:59 GMT  
		Size: 3.7 MB (3674613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a6c94d9e55e42f9e673d194aba4768ed7ec499b58cdac72c9dc5d060d3ec1`  
		Last Modified: Fri, 08 Jan 2021 19:37:02 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
