## `openjdk:17-nanoserver-1809`

```console
$ docker pull openjdk@sha256:e123a5dbcf202e37122ed2d9e18a1664a8b9a955f1f2c7e4ef6bb8d86056a987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `openjdk:17-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull openjdk@sha256:4eb1d278451a4a019144b2cc7a70bccbafdf6db81cd1f85eb80d48828cb1a538
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286198708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ef73004e44a9e881d1b8a027a71e1ae4fa5c0e2d9fbd6d667d6d82d44a28da`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 18:58:23 GMT
SHELL [cmd /s /c]
# Mon, 28 Dec 2020 21:51:26 GMT
ENV JAVA_HOME=C:\openjdk-17
# Mon, 28 Dec 2020 21:51:26 GMT
USER ContainerAdministrator
# Mon, 28 Dec 2020 21:51:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Mon, 28 Dec 2020 21:51:38 GMT
USER ContainerUser
# Fri, 08 Jan 2021 19:19:54 GMT
ENV JAVA_VERSION=17-ea+4
# Fri, 08 Jan 2021 19:20:27 GMT
COPY dir:f4566a9c0c60841d4c036675c1cd7ed02850bad16e9b2b253e3d937ea546e17c in C:\openjdk-17 
# Fri, 08 Jan 2021 19:20:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 08 Jan 2021 19:20:59 GMT
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
	-	`sha256:33b80aa1b697da500ba4c274df29d7d303143a959d616d7e5a4beedfbedf5cf7`  
		Last Modified: Mon, 28 Dec 2020 22:02:59 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ce0b0fafcb9f312707c293e822c52606813545fdf01717b420b72e20faad3c`  
		Last Modified: Mon, 28 Dec 2020 22:02:58 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4721418f9519ff146e3e520e2b942e21b0f4b1a06863f2b3de99c48542b9cdbb`  
		Last Modified: Mon, 28 Dec 2020 22:02:59 GMT  
		Size: 66.0 KB (65967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b38aab677d2fe5ff72b09e4f69954a90189cd63516578596920b168c901728`  
		Last Modified: Mon, 28 Dec 2020 22:02:55 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73678857ffa9631681c2120ae0a12579f3815da2b334902216b197e7a00a8bb4`  
		Last Modified: Fri, 08 Jan 2021 19:34:36 GMT  
		Size: 911.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59903e15b3b5a98255ebb181ddaf2d829a801a64f5d222a62174905184220f9b`  
		Last Modified: Fri, 08 Jan 2021 19:34:56 GMT  
		Size: 181.2 MB (181196877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931661468dabf7acb78810f31ef014617082f6927c2fa23ec4f303315d53948`  
		Last Modified: Fri, 08 Jan 2021 19:34:38 GMT  
		Size: 3.7 MB (3665725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b375b63c4e0c21585371f2e9c84cd822d90083147e0ce7906b9e8b7735a6d3ff`  
		Last Modified: Fri, 08 Jan 2021 19:34:37 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
