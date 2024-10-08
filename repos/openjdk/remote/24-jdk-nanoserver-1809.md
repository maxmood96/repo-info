## `openjdk:24-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:067aa5fab963fd57ef3b27a76d29f836a4d605facdd2a955dc46f866de1354fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `openjdk:24-jdk-nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull openjdk@sha256:74a7a9f64affdef6965f71a45c08f570522953d3b77b8a9cf3556f90bb9c0ae1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.7 MB (367738004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2f3867a0a164321348ea5420ba1b667d1b395d6698a8479f15bedb1137ea3e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Tue, 08 Oct 2024 00:53:26 GMT
SHELL [cmd /s /c]
# Tue, 08 Oct 2024 00:53:28 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 08 Oct 2024 00:53:28 GMT
USER ContainerAdministrator
# Tue, 08 Oct 2024 00:53:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 08 Oct 2024 00:53:42 GMT
USER ContainerUser
# Tue, 08 Oct 2024 00:53:43 GMT
ENV JAVA_VERSION=24-ea+18
# Tue, 08 Oct 2024 00:53:58 GMT
COPY dir:f5140de5e996aa4094129ad1a1d9758b1b65115ff663859b09e72bb409560f2c in C:\openjdk-24 
# Tue, 08 Oct 2024 00:54:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 08 Oct 2024 00:54:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6764225025e590506c7dbe815e01a5892be6fdd4e489980f6270e14fa53e16`  
		Last Modified: Tue, 08 Oct 2024 00:54:11 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2132c3dfc9e6531b5a737608f8b9e41091e463cf28c3420fc3e08a71eda7be0`  
		Last Modified: Tue, 08 Oct 2024 00:54:10 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac6c89637bda72b354538a05423ecaa71a565b7a36d7a159c6925e7ff8fca65`  
		Last Modified: Tue, 08 Oct 2024 00:54:10 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a0b521620e9b5994759390d4e61cc469c2740ec54f2884c829aadfffc08c91`  
		Last Modified: Tue, 08 Oct 2024 00:54:10 GMT  
		Size: 66.1 KB (66106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d9266be192c836ec739d4e77bf963a48a9209a5895a22d3f61c6c8a25e3d99`  
		Last Modified: Tue, 08 Oct 2024 00:54:09 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09c922a72c095dd279993da5e91d5cd251e18b847df1db584824c54dcb0c1fb`  
		Last Modified: Tue, 08 Oct 2024 00:54:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2925833259a1dbf498491379a066a2d51c2c072a68dad9a42b1dbd9a6877fe3`  
		Last Modified: Tue, 08 Oct 2024 00:54:20 GMT  
		Size: 208.0 MB (208000970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc33ea1daa872dd15b77c90c0682e14e94fe008259de9490b5e2ca028b40a531`  
		Last Modified: Tue, 08 Oct 2024 00:54:09 GMT  
		Size: 4.6 MB (4583659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6b48d76887f1980c6ba8ca55188c6bc88adad5b2743f445ee7fcabaed22385`  
		Last Modified: Tue, 08 Oct 2024 00:54:09 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
