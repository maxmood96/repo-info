## `openjdk:18-nanoserver`

```console
$ docker pull openjdk@sha256:064f12f749ddfceb813e466873c651debb33b5595fe41add44605dd1895d7666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `openjdk:18-nanoserver` - windows version 10.0.17763.3770; amd64

```console
$ docker pull openjdk@sha256:2ea636acf0870766dd59e54d5465115f1bf8de6a8db5a8fd350b2a07410efcb0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294636956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb47c169fcb19b3f5e35196e2aeea806ad4c13088ba74d6606eaab2d2d49a391`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Tue, 13 Dec 2022 22:53:34 GMT
SHELL [cmd /s /c]
# Wed, 14 Dec 2022 03:13:46 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 14 Dec 2022 03:13:47 GMT
USER ContainerAdministrator
# Wed, 14 Dec 2022 03:14:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Dec 2022 03:14:08 GMT
USER ContainerUser
# Wed, 14 Dec 2022 03:14:09 GMT
ENV JAVA_VERSION=18.0.2.1
# Wed, 14 Dec 2022 03:14:26 GMT
COPY dir:ee5a32dc618f3d1ccd1a23fd44bf5e8d063a799e660c0fa7a176452c3ac100ba in C:\openjdk-18 
# Wed, 14 Dec 2022 03:14:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Dec 2022 03:14:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fe06cbef5ac46e54edd743daf1bc2bfa36b294c7ce9104837061c41a4bde7b`  
		Last Modified: Tue, 13 Dec 2022 23:57:01 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bb7f87084d361e20dacad5b2e3212c102f0ed46782c8fdabe0aff837854279`  
		Last Modified: Wed, 14 Dec 2022 08:51:46 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bac56f344a2dc286ea4f4fddce5a0039df0d51574e0ced05eea2621def4ce08`  
		Last Modified: Wed, 14 Dec 2022 08:51:46 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa300866f47b1e08279528bc20d1fd29d4f72e0c9c4b674a5bd6fec673197b1c`  
		Last Modified: Wed, 14 Dec 2022 08:51:46 GMT  
		Size: 63.1 KB (63074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480982d598cb9215626d2b3c10949eff6c19f9f1ed4e08bacc014291ec9312e2`  
		Last Modified: Wed, 14 Dec 2022 08:51:44 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6c4b8d21dc14f5ca1e1583065d2f411f92305725c8e186758d2aaf1e1c43fe`  
		Last Modified: Wed, 14 Dec 2022 08:51:44 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684ad018e9480c227ebbc669a7382af0c3d6664b102adaa027d1ea95b10e9c4`  
		Last Modified: Wed, 14 Dec 2022 08:52:04 GMT  
		Size: 184.3 MB (184348915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857396d2ab4b972e87f1e00fc871c997b379ad407d29051b48bad12ea3021cd1`  
		Last Modified: Wed, 14 Dec 2022 08:51:45 GMT  
		Size: 3.5 MB (3546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c8fb4a4790961c34aab58d32656bf1162aa2589291e57e8d43e4024bf9fc39`  
		Last Modified: Wed, 14 Dec 2022 08:51:44 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
