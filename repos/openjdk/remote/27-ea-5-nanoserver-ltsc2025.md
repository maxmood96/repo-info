## `openjdk:27-ea-5-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:e7cc7c16668160d198cfae8649281f68bafd478a751370c3da8fff67e03654cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `openjdk:27-ea-5-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:b36148e82ae040dd64d4e75da15ebaa08d5ad9ef61e751231eca8c11785f1751
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.3 MB (423344166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fc97a540238f87fe110a7c2ded41d3eb9fe32fdf9c09ceb46095bacdacdb61`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 20 Jan 2026 19:10:15 GMT
SHELL [cmd /s /c]
# Tue, 20 Jan 2026 19:10:16 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 20 Jan 2026 19:10:16 GMT
USER ContainerAdministrator
# Tue, 20 Jan 2026 19:10:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 20 Jan 2026 19:10:23 GMT
USER ContainerUser
# Tue, 20 Jan 2026 19:10:24 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 19:11:18 GMT
COPY dir:2351caaa563662896c889f1c7ad17c3ab77559d0da2169277ad297474751eb8c in C:\openjdk-27 
# Tue, 20 Jan 2026 19:11:26 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 20 Jan 2026 19:11:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:56 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bb79b3f25815a4d814fa8197fc1d6952e6573864667142cd18bd7fd7d9c23c`  
		Last Modified: Tue, 20 Jan 2026 21:12:27 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6041a31509244388cc96d4b36732643d4fd474cad9778debee3c97578469b76`  
		Last Modified: Tue, 20 Jan 2026 19:12:00 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a16a10cb61455a026444501c2393871e175450e8161d710a1ec53762dc90fb9`  
		Last Modified: Tue, 20 Jan 2026 19:12:00 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d062c8c4fb694f1707a61f50c8597ebb4470661b7d663b70ad143ca4c2f51269`  
		Last Modified: Tue, 20 Jan 2026 19:12:00 GMT  
		Size: 72.4 KB (72427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dd03f409914f0d2fd15f21a60a3ce3f2812384c399dbba2d8a0c3af4bb5311`  
		Last Modified: Tue, 20 Jan 2026 19:11:35 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b8020253c57c12a8001106d743dd359673de2e44e0d1f60fdf81dfd182a31`  
		Last Modified: Tue, 20 Jan 2026 19:12:01 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce9edc95096a382dbb63e6fe197ee07b0566817f1404edc6beba29ddd4b6695`  
		Last Modified: Tue, 20 Jan 2026 19:36:43 GMT  
		Size: 224.1 MB (224064770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c2e35e6dae16540723f3b5900e94bff822174916beded5f42ce4baef336ba`  
		Last Modified: Tue, 20 Jan 2026 19:11:35 GMT  
		Size: 124.0 KB (123989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6b902aded73807fc04779e2a0a1f16a951711b1f99b610fdc6b0fdd128e50f`  
		Last Modified: Tue, 20 Jan 2026 19:11:35 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
