## `openjdk:28-ea-4-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:8cbf195c6ba2492957cc84708efdaa2ae59cf13129464105e035ac6b0c6a3f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `openjdk:28-ea-4-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

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
