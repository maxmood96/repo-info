## `openjdk:8u292-nanoserver-1809`

```console
$ docker pull openjdk@sha256:24d0e3fd7a3abde78db99e8e584501dbc489a0a232468351d6a60fb2de20b38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:8u292-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:16ca8fc19a75c45b63b50287fb9b4e0484313b22acc2d224e3d8224b6b85e33b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203939369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc8fa3ef69dcbf05adc2e0cf17508216e132904fb0b2312246f7f6cc902f119`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:53:30 GMT
SHELL [cmd /s /c]
# Wed, 14 Jul 2021 03:30:22 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Jul 2021 03:30:24 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 03:30:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Jul 2021 03:30:42 GMT
USER ContainerUser
# Wed, 14 Jul 2021 03:30:44 GMT
ENV JAVA_VERSION=8u292
# Wed, 14 Jul 2021 03:30:59 GMT
COPY dir:04533fde1b9ea0cd60bd0fd48d2f644dab91f29f3b0d8a376770cc16b38c53d2 in C:\openjdk-8 
# Wed, 14 Jul 2021 03:31:18 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d8754fb12dd351c91bed29d92c703cddb135a78d8f056b6a3bf13a251c1d2d`  
		Last Modified: Wed, 14 Jul 2021 03:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3609dce65084314b4fcdbee2b4c9cac86e4ba6a2f6731228036cb6d732decda9`  
		Last Modified: Wed, 14 Jul 2021 03:58:13 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beea74f08cf2d09382b86b1680d8741d756d6136a94cbad80c4521348f4999d4`  
		Last Modified: Wed, 14 Jul 2021 03:58:13 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a284e1f3d144cb79b4c435ae2a981fcfdb8c8dc7e29dc1a4ca3fc1df81e5ff`  
		Last Modified: Wed, 14 Jul 2021 03:58:11 GMT  
		Size: 67.4 KB (67382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501cb4cf39ea8969b47e4aec6a12c620974aefe7be361eb0a17f5cd081fbeb90`  
		Last Modified: Wed, 14 Jul 2021 03:58:11 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512db6d893615b217cc11cbfe7b021240f92c66921326c18cabe10984c703b9`  
		Last Modified: Wed, 14 Jul 2021 03:58:11 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33dae0b19316e3d96c138e35dedbdc99e31c71c980cbe1f8a5e92ffe5356f23f`  
		Last Modified: Wed, 14 Jul 2021 03:58:23 GMT  
		Size: 101.0 MB (101039290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bc08d1c679d613227d19733d188c2bc4816f626a88e92688eaa1708a0fea0e`  
		Last Modified: Wed, 14 Jul 2021 03:58:11 GMT  
		Size: 101.3 KB (101298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
