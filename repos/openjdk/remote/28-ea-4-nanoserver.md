## `openjdk:28-ea-4-nanoserver`

```console
$ docker pull openjdk@sha256:3d35823ae7fe4400c91a62345735ee0ab40e98867e4c1b69f8a703823f7d5a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `openjdk:28-ea-4-nanoserver` - windows version 10.0.26100.32995; amd64

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

### `openjdk:28-ea-4-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:0406f22d2b88d9dbeda124c964c9949d4800985de93a417bf2bddaccbc277005
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.2 MB (348223078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0aff122af1fb687186f57544a3efdbe5d9f854e354c4c248e60df7dadfb0262`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Fri, 26 Jun 2026 23:08:56 GMT
SHELL [cmd /s /c]
# Fri, 26 Jun 2026 23:08:57 GMT
ENV JAVA_HOME=C:\openjdk-28
# Fri, 26 Jun 2026 23:08:57 GMT
USER ContainerAdministrator
# Fri, 26 Jun 2026 23:09:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 26 Jun 2026 23:09:04 GMT
USER ContainerUser
# Fri, 26 Jun 2026 23:09:05 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 23:09:25 GMT
COPY dir:eef968aefc3beb427e11070e56ba6cc1188ab5370b0606d52ca8b4a8548d912f in C:\openjdk-28 
# Fri, 26 Jun 2026 23:09:29 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 26 Jun 2026 23:09:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed77d180d477cbb985a6390cd46db954f0e316f48a4a126677cb92ef04d13a1`  
		Last Modified: Fri, 26 Jun 2026 23:09:35 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623bdba95e1a6e6842530f33ef12a3497a72c5c6e899590532e366b269d039ee`  
		Last Modified: Fri, 26 Jun 2026 23:09:35 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad73367b2cf8b9e659bd6fc3d1908b92a468658482581b3d6a8a6040093338a`  
		Last Modified: Fri, 26 Jun 2026 23:09:35 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4eb594f07f477b05be3a1aa28ecb59fd677ff717c480e20eb3ea1e844cce9d`  
		Last Modified: Fri, 26 Jun 2026 23:09:35 GMT  
		Size: 77.5 KB (77507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a61539f982491917818e0e64aa12d16cafc758a74910dceb9ab3010d03582f`  
		Last Modified: Fri, 26 Jun 2026 23:09:33 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7229274eefc477dd4a40c2a0296d0914426b2a7847013bd283da388abd04b0`  
		Last Modified: Fri, 26 Jun 2026 23:09:33 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3484763d5f10e40ffd5ece415647032a8a45705120601e10d96acc6643c8b1d4`  
		Last Modified: Fri, 26 Jun 2026 23:09:49 GMT  
		Size: 224.0 MB (224046873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0320b3c102fce1b205fa237174d4fc3031ba78f748589bfe1539cc644813d817`  
		Last Modified: Fri, 26 Jun 2026 23:09:33 GMT  
		Size: 94.9 KB (94872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4495188fae51f13cacf10c54d118063bf4ff230854ab59c3771f097ddd3cb7c`  
		Last Modified: Fri, 26 Jun 2026 23:09:33 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
