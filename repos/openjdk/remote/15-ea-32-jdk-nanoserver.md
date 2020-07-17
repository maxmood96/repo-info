## `openjdk:15-ea-32-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:dc922e7397d0855b8cab2d5d55ddc1ead412a66dd5c6a71d237685ac85a82dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:15-ea-32-jdk-nanoserver` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:127f42f89ab72a9aa32d760ba7ea63f158607f850d86141bd9b7db2b3cc04afb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295811047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f62b7c174c50333720d51199c39949bd837b192f80c911811d84010a50d348`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Jul 2020 13:50:07 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jul 2020 01:54:43 GMT
SHELL [cmd /s /c]
# Wed, 15 Jul 2020 02:03:33 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 15 Jul 2020 02:03:34 GMT
USER ContainerAdministrator
# Wed, 15 Jul 2020 02:03:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 15 Jul 2020 02:03:45 GMT
USER ContainerUser
# Thu, 16 Jul 2020 23:16:12 GMT
ENV JAVA_VERSION=15-ea+32
# Thu, 16 Jul 2020 23:17:06 GMT
COPY dir:9a408333ef17b4adde7a64c7992c499e7d89ae3afb0f7cb5bee220acfc08242f in C:\openjdk-15 
# Thu, 16 Jul 2020 23:17:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 16 Jul 2020 23:17:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dc95608099543221ef539391bfece5c1ce37b97af9da457f5990349cab028a12`  
		Size: 100.9 MB (100895619 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f6486e4debac36806ed3527d9b1baea75c1a807e26baccdd0a2f521c814273f`  
		Last Modified: Wed, 15 Jul 2020 02:43:55 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17195adca743b283e9fdf01c1670d33e88c1b7f8ad0ff6a19afa11f90abbdaa`  
		Last Modified: Wed, 15 Jul 2020 02:46:29 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4978cbb8680255360d757c7d46e5a1c7c246047f93257964335958cd1b1307`  
		Last Modified: Wed, 15 Jul 2020 02:46:30 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a772f899b85a5ec3b1356709ac25974f0b40a2729a3b6bd12f56e44a5cee769d`  
		Last Modified: Wed, 15 Jul 2020 02:46:29 GMT  
		Size: 67.3 KB (67317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29415bb95c60f5fdec327237a6683b4a710b6cf5925d41adef8d21f8a277140e`  
		Last Modified: Wed, 15 Jul 2020 02:46:26 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315fb90be87687774e3ce95db7f879c651dfb0561d6253c805b85fd33f96eb96`  
		Last Modified: Fri, 17 Jul 2020 00:21:37 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8ed07ca01923cb7f6bd3c3642df1ae69aae4d1065febee9281df6bdac9177`  
		Last Modified: Fri, 17 Jul 2020 00:21:56 GMT  
		Size: 191.4 MB (191358498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e926e4ceaf0785ad77c752eabed3862adf2516d6a5102229afe75e0f01934ad`  
		Last Modified: Fri, 17 Jul 2020 00:21:38 GMT  
		Size: 3.5 MB (3484270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e634c0f4a588e180ebcb3f7113fc7b34bf5ee283b1f4e49614616d9a5facbfe2`  
		Last Modified: Fri, 17 Jul 2020 00:21:37 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
