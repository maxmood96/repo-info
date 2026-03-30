## `openjdk:27-ea-15-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:f36ca374b0c687a92dec9c0c398789d8d859e2941028495b8dba04a623c486b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `openjdk:27-ea-15-nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:adcd88855b2d4f4c5697f7c1a9ec132ac8c759786a31480a0048f417ffdc1cbd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (424045009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762e97d0e4391d21acaaa1e4ad83e5840efa4ec0cc349127a5baaf4f559773e8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Mon, 30 Mar 2026 18:29:14 GMT
SHELL [cmd /s /c]
# Mon, 30 Mar 2026 18:29:14 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 30 Mar 2026 18:29:15 GMT
USER ContainerAdministrator
# Mon, 30 Mar 2026 18:29:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 30 Mar 2026 18:29:27 GMT
USER ContainerUser
# Mon, 30 Mar 2026 18:29:28 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 18:30:47 GMT
COPY dir:a373531bc68615ea541aa6fcf8d3b8dbeba3f73235aedbbf62e1427c8271e4d6 in C:\openjdk-27 
# Mon, 30 Mar 2026 18:30:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 30 Mar 2026 18:30:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b45ed1c30db2e84fb0e26f03b644c5f7c878bf7d108df85478bba0b4c21d13`  
		Last Modified: Mon, 30 Mar 2026 18:31:04 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b6bf5659bc433d87c52a88c1f62e7e90779c7bb21e242161c1d0b9e4c1ca2f`  
		Last Modified: Mon, 30 Mar 2026 18:31:04 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43085ee1674ed3d1492b595d77489570c7bbb3e700204825bfc751c7d130e91`  
		Last Modified: Mon, 30 Mar 2026 18:31:04 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54e3d80729f31232b93b9c43639d0ce02cff73c47815b24c95bdaaebb0e0cc9`  
		Last Modified: Mon, 30 Mar 2026 18:31:04 GMT  
		Size: 70.2 KB (70207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23879ce013923f1c3a9a753def3c54bd05be649949568b004728e9a749dc739e`  
		Last Modified: Mon, 30 Mar 2026 18:31:03 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537e7944538f0fc92a6d285f33b20bd67a5723c7790e3bd7aae04dcad701c098`  
		Last Modified: Mon, 30 Mar 2026 18:31:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2810607d53778a58879e3bb80836f0c9ca56a0cb44ef56e8897e898c82b74a`  
		Last Modified: Mon, 30 Mar 2026 18:31:17 GMT  
		Size: 224.4 MB (224436469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260de0725a58217b9c7e5f8dfbb843c6e9c659f8726822e336e5cb8f136534dc`  
		Last Modified: Mon, 30 Mar 2026 18:31:03 GMT  
		Size: 122.6 KB (122553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96a11b2a09a6653bad40c40b95f492deefcbffc2f581b1a10d6581c1bfe94d0`  
		Last Modified: Mon, 30 Mar 2026 18:31:03 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
