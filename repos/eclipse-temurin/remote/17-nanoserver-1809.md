## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:51d1e72adcbda216fd2b67d70cba7536fd754b74dcceab6b9e3f55844b122ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:1e465d28cdd0beddb8cde35ca5ee92a5a3daf0275fd9479f00ec52d08641cc80
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347268411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a823a83e8b388283a33ffedd37ac1cbaf6314f0c120b23f0b357f6bfea4642d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:54:50 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 17:54:51 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 15 Jan 2025 17:54:51 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 15 Jan 2025 17:54:52 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 17:54:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 17:54:54 GMT
USER ContainerUser
# Wed, 15 Jan 2025 17:55:01 GMT
COPY dir:52d780064906626480ed3e0e10c20681fda9fbf2926de2858bcee46524c2c3aa in C:\openjdk-17 
# Wed, 15 Jan 2025 17:55:06 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jan 2025 17:55:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45bcd7c9b59ff3db2f91eb2b8bb2cd92b1896708f53c56904dd8287837eca93`  
		Last Modified: Wed, 15 Jan 2025 17:55:13 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623944b481f83aaad6ccb0693e07226409ba0376c26604e631fea7dcad843cee`  
		Last Modified: Wed, 15 Jan 2025 17:55:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33069a22dfb29a79372e61861f08168103b0fe16ffd51082aa6a923040a32e33`  
		Last Modified: Wed, 15 Jan 2025 17:55:12 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765a65dec6f570a4f95356120cad3d45801e86bf816ee56444701601639e9875`  
		Last Modified: Wed, 15 Jan 2025 17:55:12 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4559b6df6a7b4442c0841e7e4a8c28b48479923adc8e31df0c5f894c0bb30ec4`  
		Last Modified: Wed, 15 Jan 2025 17:55:10 GMT  
		Size: 72.2 KB (72184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e639da243ffe28a8780e309af93e71cfc8715507a3340f8d8a8a858616fe08`  
		Last Modified: Wed, 15 Jan 2025 17:55:10 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61cbe3b3a5b3111f3440803cde370ae329796513010205f2466a45ae923a4e6`  
		Last Modified: Wed, 15 Jan 2025 17:55:20 GMT  
		Size: 188.3 MB (188301058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7296046628b17a9138021932d78791313d819608dc8770095af2dfb974c6be30`  
		Last Modified: Wed, 15 Jan 2025 17:55:11 GMT  
		Size: 3.6 MB (3621363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a70892ac227898182f9c6b5c7e78a15f405def79900beda472d1061963ff33`  
		Last Modified: Wed, 15 Jan 2025 17:55:10 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
