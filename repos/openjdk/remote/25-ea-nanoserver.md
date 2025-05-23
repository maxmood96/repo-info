## `openjdk:25-ea-nanoserver`

```console
$ docker pull openjdk@sha256:8fff2b5f599dce3ff9a86baa6bf2ec752af3094028a17785d4093d1ef10e48a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.17763.7314; amd64

### `openjdk:25-ea-nanoserver` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:de92fc1744a65eeeddaff5dd95309b164c1876ff0c16fa5f4c1b6a8ab3a85c1e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.9 MB (400942552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7893029e17389ccd0f0012da311b6ab4eb842484f5e47253e4c73b7587e1cd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Fri, 23 May 2025 20:13:11 GMT
SHELL [cmd /s /c]
# Fri, 23 May 2025 20:13:12 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 23 May 2025 20:13:13 GMT
USER ContainerAdministrator
# Fri, 23 May 2025 20:13:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 23 May 2025 20:13:16 GMT
USER ContainerUser
# Fri, 23 May 2025 20:13:17 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 20:13:24 GMT
COPY dir:d32a1e622c307f990d42f1dfe6052e231c098d4b948c30b3def65fbe5914b454 in C:\openjdk-25 
# Fri, 23 May 2025 20:13:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 23 May 2025 20:13:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Tue, 13 May 2025 23:02:56 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da2e7ca37ec8067c7ec8d6cab286ef187443fbf8625888ec227b4ba5ade1a36`  
		Last Modified: Fri, 23 May 2025 20:13:38 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f058980b6ff436a54f373d5a953732601b094d1a0854191a6e83688219214d79`  
		Last Modified: Fri, 23 May 2025 20:13:38 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53536315e774643720364354ae5d97d41bb1cb77e24755675149a4bb3672215c`  
		Last Modified: Fri, 23 May 2025 20:13:37 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc06808f8483b763ccbfd31d2583cc388c6af5d8c5579b159aaeae4167c4a57`  
		Last Modified: Fri, 23 May 2025 20:13:37 GMT  
		Size: 76.3 KB (76298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658021efa7f52f0a6ce0061ab2bd2c8d197d3266a56b106e48dacbc1f4b9117e`  
		Last Modified: Fri, 23 May 2025 20:13:36 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41233b75940eacf560efca8c2021a6b4e6d3a4a488185c116c9ab8b87b9a1a3b`  
		Last Modified: Fri, 23 May 2025 20:13:35 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe506b2a635fdfb165b908a45627c01f275d3599944542fd1eed695fcfed5ac`  
		Last Modified: Fri, 23 May 2025 20:13:47 GMT  
		Size: 209.3 MB (209333757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ef3dfe9796548c729b0cd1f6790b55b97ddc5b6c9f2ae15bfd2cf793a09339`  
		Last Modified: Fri, 23 May 2025 20:13:36 GMT  
		Size: 114.2 KB (114170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd4b37ba75fdeb73658e9f3c9e58541d4aa9fa0609f3dad9b38ee1f8afe6daa`  
		Last Modified: Fri, 23 May 2025 20:13:36 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull openjdk@sha256:6ca070e8a8a2e5e19c07321cc5c2377b6fd6b88f593e850f98a9ac7fd66bbd82
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322630738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5b2c8d965f88e6e265808b704b96fb609732ee00c38ba43c0727ea39ad220e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Fri, 23 May 2025 20:11:08 GMT
SHELL [cmd /s /c]
# Fri, 23 May 2025 20:11:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 23 May 2025 20:11:10 GMT
USER ContainerAdministrator
# Fri, 23 May 2025 20:11:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 23 May 2025 20:11:13 GMT
USER ContainerUser
# Fri, 23 May 2025 20:11:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 20:11:21 GMT
COPY dir:d32a1e622c307f990d42f1dfe6052e231c098d4b948c30b3def65fbe5914b454 in C:\openjdk-25 
# Fri, 23 May 2025 20:11:27 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 23 May 2025 20:11:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4a7060407f6f2202ac8da0d62a335eaa0a30c03245c43c623c3175fa13973`  
		Last Modified: Fri, 23 May 2025 20:11:34 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169a032d4a714eab189784eaec4d78c59225be316ecbc1133c076b03eb02eb5d`  
		Last Modified: Fri, 23 May 2025 20:11:33 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256bbf346ee3e469c3d1f400b79de0852273219ec1bc9c66c0891f04954741ba`  
		Last Modified: Fri, 23 May 2025 20:11:33 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cb4a4fc858db0cd44cf3870fb0b45c6420befbafcb3af70a306311d30ae450`  
		Last Modified: Fri, 23 May 2025 20:11:34 GMT  
		Size: 68.8 KB (68810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c93655e3fb8db4251ed8b7fa8d0a44940bd4f4db04c339e66667f5ceccae494`  
		Last Modified: Fri, 23 May 2025 20:11:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6264f4235ae8c6b5f855b56c6bf58188c743a0aca5b8c216289b1180f2005dac`  
		Last Modified: Fri, 23 May 2025 20:11:32 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff46d848a1caf39970e1887399504a260fa71b0ae8f9d402b6e7dd13e8648adb`  
		Last Modified: Fri, 23 May 2025 20:11:43 GMT  
		Size: 209.3 MB (209333948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56eb33e20f0982063e73c5464c0765fd44b1fe908af0fb65e6b99ec5acbbcd52`  
		Last Modified: Fri, 23 May 2025 20:11:32 GMT  
		Size: 4.4 MB (4441185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd679f8d4b7d4dba3b31d995803823e6475ceba47d1bdbdbc4e59caa3f01eeb`  
		Last Modified: Fri, 23 May 2025 20:11:32 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
