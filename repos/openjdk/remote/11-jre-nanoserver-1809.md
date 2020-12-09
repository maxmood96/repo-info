## `openjdk:11-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:43ebaf99afabe8555484b9dde0f050eee5568292827aee857bdca499e99088ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `openjdk:11-jre-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull openjdk@sha256:dd760d8fad1fbc1de68e69c403936b2bd2305d0538858e895d1cbbfdaf1ad076
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140716322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d646d39a0a29661202002c7e3c999a8cfd644903f114342a7a764462d9f19242`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 18:58:23 GMT
SHELL [cmd /s /c]
# Wed, 09 Dec 2020 19:14:02 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Dec 2020 19:14:03 GMT
USER ContainerAdministrator
# Wed, 09 Dec 2020 19:14:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 09 Dec 2020 19:14:14 GMT
USER ContainerUser
# Wed, 09 Dec 2020 19:14:15 GMT
ENV JAVA_VERSION=11.0.9.1
# Wed, 09 Dec 2020 19:18:27 GMT
COPY dir:eaef7c5ff292e1f8a6aa3c608a2a96aef7062e71406091a23afb53db379465e6 in C:\openjdk-11 
# Wed, 09 Dec 2020 19:18:42 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fe9a51a0164bd1c063cbda08c4e22dc4f5d04a8047a3951d7441f37fb93c57f2`  
		Last Modified: Wed, 09 Dec 2020 19:34:04 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0681bab6753ceecaa7ad1fe6c2d487992cbc05d43923edc37840bf023d6cb99a`  
		Last Modified: Wed, 09 Dec 2020 19:39:17 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c8b4aea06465f7033f439329ba26085a17c8edfc5b8bcd4b70a47c41b7bad4`  
		Last Modified: Wed, 09 Dec 2020 19:39:17 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0056bcc8e2e29b6161602faba9c17d21988ed24e7601571fd93b11023fb2f523`  
		Last Modified: Wed, 09 Dec 2020 19:39:17 GMT  
		Size: 64.2 KB (64245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0016925aef0422a4746cb39257e07e38e66756014da54f003bdcff05e02394`  
		Last Modified: Wed, 09 Dec 2020 19:39:14 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f9048a27002c34d0a8b60583ebdaa9655fc644e45b6030d74155731012510`  
		Last Modified: Wed, 09 Dec 2020 19:39:14 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac260580a769e7ed24862c4fe67e975cd7bed262c560ecfe8beeeb802804334`  
		Last Modified: Wed, 09 Dec 2020 19:47:08 GMT  
		Size: 39.3 MB (39306638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6978a82a263991e503cf26f295efa4cfbbf37d4f794a8477cf11d14c39410b26`  
		Last Modified: Wed, 09 Dec 2020 19:47:02 GMT  
		Size: 76.2 KB (76243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
