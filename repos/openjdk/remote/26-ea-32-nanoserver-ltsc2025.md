## `openjdk:26-ea-32-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:3501706906f3838851380c1eea91422a7eb7dd29de1026d6611d0dfed1b4f6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `openjdk:26-ea-32-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:fe562de07ccd8562fa89e5fea13dff2cfd6de3f222c98b6d534ce0afc96038c0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.1 MB (423137948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7ff21a4cc49e4f547e3e7eb60b529c3cfe77d700cf4e73a8e738cda98a741c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 23:14:32 GMT
SHELL [cmd /s /c]
# Mon, 26 Jan 2026 23:14:33 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 26 Jan 2026 23:14:34 GMT
USER ContainerAdministrator
# Mon, 26 Jan 2026 23:14:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 26 Jan 2026 23:14:50 GMT
USER ContainerUser
# Mon, 26 Jan 2026 23:14:50 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 23:15:51 GMT
COPY dir:1413f25fe2f5e950fbcb1d8e8eb2b3797092a9f87fa5ca5a59c32e02bcbf5aa0 in C:\openjdk-26 
# Mon, 26 Jan 2026 23:15:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 26 Jan 2026 23:16:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74493d4c21d3e461dd7771e25d955e7b6118e4fd340867797772590825897fd3`  
		Last Modified: Mon, 26 Jan 2026 23:16:06 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a88d75405661795412f610531386bec6c4faa99a80d858ac320871a9a87853`  
		Last Modified: Mon, 26 Jan 2026 23:16:06 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd910c52886a56829cd98cc7b24acfdfdf0ec1ffcc29e530b3435f386d0f2b6`  
		Last Modified: Mon, 26 Jan 2026 23:16:06 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1525acad8aa409679e47da30c037055474d19f6c52f2a231cb0342a40d4e864`  
		Last Modified: Mon, 26 Jan 2026 23:16:06 GMT  
		Size: 73.1 KB (73093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb08faaa34c79ee47fa7e2a6390d5118c46ca0919eb3ed1132180680d68cad1`  
		Last Modified: Mon, 26 Jan 2026 23:16:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cfda236d39b5182dfd108ea1521f7e17ed89b756756c60376205db820c59dd`  
		Last Modified: Mon, 26 Jan 2026 23:16:04 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ef1a377a6861bccdda07f8c21b190cabbbe6b445722a95e60f4240368f0cb`  
		Last Modified: Mon, 26 Jan 2026 23:16:21 GMT  
		Size: 223.9 MB (223878347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27c219e63306d8a36faba3e9869563f653cc0ddcbe7411994d8df49a8e173f0`  
		Last Modified: Mon, 26 Jan 2026 23:16:05 GMT  
		Size: 103.5 KB (103523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce0eef41ca548e46e6a56ffae3fea3b21d93646c1374af14862f0f2ed66f57f`  
		Last Modified: Mon, 26 Jan 2026 23:16:05 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
