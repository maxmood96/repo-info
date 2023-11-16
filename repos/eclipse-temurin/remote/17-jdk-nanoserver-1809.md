## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:8daccb7636c45d9ee1d0c508613bd33eac5a65e4f3b3113c960b24e06a74defb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull eclipse-temurin@sha256:bd4ceed92c590c70928e55a6415a86668481a15106bb45a416a93cd7bed8dbbc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294845790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c466e61a11eb20fced173642f4e6bd61cd88bebe19f97b1b27c34508f72b7b6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 01:41:12 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 02:01:51 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Thu, 16 Nov 2023 02:01:52 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 16 Nov 2023 02:01:53 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:02:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 02:02:02 GMT
USER ContainerUser
# Thu, 16 Nov 2023 02:02:17 GMT
COPY dir:abd8f71dbffdebb78ff7b01992fc9930e8aa0c6f2b1d8e6ad05b2a0c8da5ed1e in C:\openjdk-17 
# Thu, 16 Nov 2023 02:02:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Nov 2023 02:02:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5c133738aab79d4c21c47e77cb838e2d00166f5e3e2632177622f67488259`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a929d328ae624d5b0c26b2c6080f8fadda432a89348c53c823ead3ea83cb31ad`  
		Last Modified: Thu, 16 Nov 2023 02:33:28 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e523d409cba7796d6a2c3d60186d4504d38d430101cd5cdb583608c12fa3322d`  
		Last Modified: Thu, 16 Nov 2023 02:33:28 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5b00068b929a533e7e5f34941b1ff74b39efd9132278ffb636df385fdfe49e`  
		Last Modified: Thu, 16 Nov 2023 02:33:27 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69e1e253770e264976b8ecead34937818726e856ce67e8d5089d0979c58a53e`  
		Last Modified: Thu, 16 Nov 2023 02:33:26 GMT  
		Size: 68.3 KB (68316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184fd96217640a6a7136df3c143c18364cb4976aa0a3368dc067d7a12bba7a7`  
		Last Modified: Thu, 16 Nov 2023 02:33:26 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ded094ef7d43c470cd8bab535808b099a646fc9130daeeed8f7301df08255e7`  
		Last Modified: Thu, 16 Nov 2023 02:33:44 GMT  
		Size: 186.7 MB (186659790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee3583c680d0c38e6fea8f26b393ced228312f599a9b7b4e8feff1e3742cf52`  
		Last Modified: Thu, 16 Nov 2023 02:33:27 GMT  
		Size: 3.6 MB (3613349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fb893da695c0441db79e350971321d98af12615e711c7a7b89cb126e39ce8`  
		Last Modified: Thu, 16 Nov 2023 02:33:25 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
