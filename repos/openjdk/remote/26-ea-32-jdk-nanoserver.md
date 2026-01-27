## `openjdk:26-ea-32-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:cf0f62f404a741613c8219b72cd8aef014d556f64f7b890f5e8f4677f9ecba6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-32-jdk-nanoserver` - windows version 10.0.26100.32230; amd64

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

### `openjdk:26-ea-32-jdk-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:d41a4e9c53012ba1f629148f501fbcc8475bc74ed9fa9ce515ef3a122e28a3f8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350788778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3226dcb1033457f04f6930de2e3e1e1d4a840877d2b1d4f2a67d5634d16cd2e6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Mon, 26 Jan 2026 23:12:36 GMT
SHELL [cmd /s /c]
# Mon, 26 Jan 2026 23:12:39 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 26 Jan 2026 23:12:40 GMT
USER ContainerAdministrator
# Mon, 26 Jan 2026 23:12:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 26 Jan 2026 23:12:54 GMT
USER ContainerUser
# Mon, 26 Jan 2026 23:12:55 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 23:14:08 GMT
COPY dir:1413f25fe2f5e950fbcb1d8e8eb2b3797092a9f87fa5ca5a59c32e02bcbf5aa0 in C:\openjdk-26 
# Mon, 26 Jan 2026 23:14:15 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 26 Jan 2026 23:14:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e51f20a630010d929dc6108e426f6d138555f634eb15711b6e888053888c8f`  
		Last Modified: Mon, 26 Jan 2026 23:14:23 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dabdd7f6091b020304e60a143feba4078aeb0d2f0f6593cf2a6fe20d93ae847`  
		Last Modified: Mon, 26 Jan 2026 23:14:23 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186cf8d9c9fffc47ad73bad0507de72a5a0d79669c233c6840d62cbe33ff1c6c`  
		Last Modified: Mon, 26 Jan 2026 23:14:22 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0eb7cf4adad6ba80ee6f5fc06d7baed3227262cbcf29fa659a1d182c0fc45`  
		Last Modified: Mon, 26 Jan 2026 23:14:22 GMT  
		Size: 75.1 KB (75113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb2cdc257cce10bc68d9da6b2cd64adbdfe6d713a96659382f51db39889a85`  
		Last Modified: Mon, 26 Jan 2026 23:14:21 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510a1f982da878ab59836274536e431e01b41053e371e83a08eb3a4558c757f0`  
		Last Modified: Mon, 26 Jan 2026 23:14:21 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394f2ad9c38010e72abc73292805c8635dd5fb617d53d2d3894cc8596d3e1620`  
		Last Modified: Mon, 26 Jan 2026 23:14:36 GMT  
		Size: 223.9 MB (223878435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dba2a242631046553bd0e3179a34563a167eb832742911d9f272598c382819`  
		Last Modified: Mon, 26 Jan 2026 23:14:21 GMT  
		Size: 132.0 KB (131954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18bdca7291a08e420fb51ad0f90cd29651ce8f0a4ee83d24b2dc9b8b7b112a2`  
		Last Modified: Mon, 26 Jan 2026 23:14:20 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
