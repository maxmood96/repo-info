## `openjdk:25-ea-21-nanoserver-1809`

```console
$ docker pull openjdk@sha256:1432815d9d096d7297823445a4a9858db7a3e9b2efaf77241de22661761f1b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-ea-21-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:231a829db0c31764d77d2f78fee0de7562dfd5d3390188bb4adca95e778027ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322347869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f954adc5055b7f675358b23cd9aee795f87ab5757d4bea43a445942ab1bda8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Mon, 05 May 2025 18:10:18 GMT
SHELL [cmd /s /c]
# Mon, 05 May 2025 18:10:19 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 18:10:19 GMT
USER ContainerAdministrator
# Mon, 05 May 2025 18:10:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 05 May 2025 18:10:29 GMT
USER ContainerUser
# Mon, 05 May 2025 18:10:29 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 18:10:41 GMT
COPY dir:38c9db30a8dff81edae6bd00112f30e7c6eed8d0f73c59888875d8c30a4a8de1 in C:\openjdk-25 
# Mon, 05 May 2025 18:10:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 05 May 2025 18:10:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce93b8eafc58c0c9e0fe40d1f12a473525c44e9813d498c5aad120415a54a89a`  
		Last Modified: Mon, 05 May 2025 18:10:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88de9bb883edfe317e9c2f63b3bd934348f944f4d71145b3c29a68b2df9a4a01`  
		Last Modified: Mon, 05 May 2025 18:10:52 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b1938e7872143a2fd9bc282154b39aef3b780726ab03ad2b3eafc156cc41e3`  
		Last Modified: Mon, 05 May 2025 18:10:52 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0a4c54e0abd44ef849e65aea191b0062c17280cd2e30cbe7e34d926079f5fc`  
		Last Modified: Mon, 05 May 2025 18:10:52 GMT  
		Size: 64.2 KB (64231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87c17ca7ad0b9c5353087f739967e7467232351872c9b6d902de3d0adf154bc`  
		Last Modified: Mon, 05 May 2025 18:10:50 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b050ebfe696340ad823d8805ebf9ecdaf44660d657be1aac7e036c42c1dcb7e0`  
		Last Modified: Mon, 05 May 2025 18:10:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67799c804181d88a2cf0e361138443dfdfa20922755b753f6050f176fda35b25`  
		Last Modified: Mon, 05 May 2025 18:11:02 GMT  
		Size: 208.8 MB (208848831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91410ef755ac4abf7f8195f4a16c0f6d350d0deedb874b7a13dc78525b3eed6c`  
		Last Modified: Mon, 05 May 2025 18:10:51 GMT  
		Size: 4.7 MB (4676291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fa446cb2c7396927227c1b625da1e13a4da6115320c03f8a43c6892ae02ed0`  
		Last Modified: Mon, 05 May 2025 18:10:50 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
