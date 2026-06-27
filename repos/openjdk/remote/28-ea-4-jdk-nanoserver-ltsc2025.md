## `openjdk:28-ea-4-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:a10de1ca9241f18e4edcfd0b8bf471726888ec91e5e1f1a43e556e5d285f8bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:28-ea-4-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:23cc0468222148f5baaeb49d4e6118a7596e4b0024d8f6e09bd7e7872e6dce43
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.9 MB (420882951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6712f30d10d23fe27929d57910fadaff0932449ae045a06ecadeed603fe9c950`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Fri, 26 Jun 2026 23:08:51 GMT
SHELL [cmd /s /c]
# Fri, 26 Jun 2026 23:08:51 GMT
ENV JAVA_HOME=C:\openjdk-28
# Fri, 26 Jun 2026 23:08:52 GMT
USER ContainerAdministrator
# Fri, 26 Jun 2026 23:08:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 26 Jun 2026 23:08:58 GMT
USER ContainerUser
# Fri, 26 Jun 2026 23:08:59 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 23:09:30 GMT
COPY dir:eef968aefc3beb427e11070e56ba6cc1188ab5370b0606d52ca8b4a8548d912f in C:\openjdk-28 
# Fri, 26 Jun 2026 23:09:36 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 26 Jun 2026 23:09:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01adf8ea0a07c7ff7204a00bee499432d9df99499d357287246716db8c9b290e`  
		Last Modified: Fri, 26 Jun 2026 23:09:43 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ab06fc1729e442e7e051ed46c49795913e8b18243be42b8677a047d2db9874`  
		Last Modified: Fri, 26 Jun 2026 23:09:43 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daccf4cbc0c1f80d93ec34bb55bccbe3f7ad6c9048534f04e1c8992c967394c8`  
		Last Modified: Fri, 26 Jun 2026 23:09:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222a5115a5aabd22b6e0b12ebe021c4c20cd008e7ee3f5c722592b8a412591e7`  
		Last Modified: Fri, 26 Jun 2026 23:09:43 GMT  
		Size: 70.0 KB (69959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45eb7c2027315fa86596fd8978d413ec36e1ee2ccc4f3e851e0fdcbf3c21618`  
		Last Modified: Fri, 26 Jun 2026 23:09:41 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1d0217e3b347eec49a566e08703ae498c5af3a4f52557e9da54c5e28bb1f7b`  
		Last Modified: Fri, 26 Jun 2026 23:09:41 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f7d278774d6af3591a8cc7fe90e8df1898b389b5f750b206740d8df6fd0838`  
		Last Modified: Fri, 26 Jun 2026 23:09:58 GMT  
		Size: 224.0 MB (224047495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1412bcea09e604017d5e87940176d7e7b391787af69306b29d1eeffe15d2a`  
		Last Modified: Fri, 26 Jun 2026 23:09:41 GMT  
		Size: 91.2 KB (91153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f155918582855f1604702ebbca37a61c2262475bdb1b01109cd379543c6994`  
		Last Modified: Fri, 26 Jun 2026 23:09:41 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
