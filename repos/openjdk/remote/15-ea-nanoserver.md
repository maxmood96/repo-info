## `openjdk:15-ea-nanoserver`

```console
$ docker pull openjdk@sha256:aab971aef9684af612d2e61bd4969a9cd38989a5c4342eaf10277089bdb3b8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:15-ea-nanoserver` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:9c5a16bb482a8994037bbe219b903ab6eaa67a7858bcdd9bc851fb3d7e88be51
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298475189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b6858d0d5c8e8f7c4d934ea3f4f324d683e17b5a379458c04d60863a9b8c83`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Tue, 14 Jan 2020 23:56:11 GMT
SHELL [cmd /s /c]
# Tue, 14 Jan 2020 23:56:12 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 14 Jan 2020 23:56:13 GMT
USER ContainerAdministrator
# Tue, 14 Jan 2020 23:56:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 14 Jan 2020 23:56:31 GMT
USER ContainerUser
# Tue, 14 Jan 2020 23:56:32 GMT
ENV JAVA_VERSION=15-ea+4
# Tue, 14 Jan 2020 23:57:39 GMT
COPY dir:83afa8f8ba97f8f7954d098b7288b36f82237e572f47d666b37c7504511161ab in C:\openjdk-15 
# Tue, 14 Jan 2020 23:57:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Tue, 14 Jan 2020 23:58:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:764e25aa4e95684bd69a4d130dc1c729bfaef95293d9c76c4d2a12ced9e3a9ac`  
		Last Modified: Wed, 15 Jan 2020 01:51:06 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f193e511d66e393e8623d9efd86f48f82cc15ceb19ee3a6ac9da7343da044ad`  
		Last Modified: Wed, 15 Jan 2020 01:51:04 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fab357b0406f3be040eca20b497e3bdd7e731b95865fbfbe83acf826248583`  
		Last Modified: Wed, 15 Jan 2020 01:51:03 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fed5c1fef1ff77da19cbdb310981f89c791b7c4206a8b99d9a1f114b6a5a107`  
		Last Modified: Wed, 15 Jan 2020 01:51:03 GMT  
		Size: 70.0 KB (69974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dae8d73c31bd6bb443dd054e2ff7514c3f89f2252ad8f45b02d272a63de3194`  
		Last Modified: Wed, 15 Jan 2020 01:51:01 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b723f17c56c90da1678c4a9f3acd1fcfe51e66966c9eb5ab4dc36680fdb102fe`  
		Last Modified: Wed, 15 Jan 2020 01:51:01 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251dcb3cb2e2fab23f239b0daa76ea6e8a5934e0269e5c1413dd53874f43cf5c`  
		Last Modified: Wed, 15 Jan 2020 01:54:25 GMT  
		Size: 193.9 MB (193900464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817e69fec93a5d36ef4b30dff0baa16da8817614031de57bdb848441f66ced03`  
		Last Modified: Wed, 15 Jan 2020 01:51:04 GMT  
		Size: 3.4 MB (3444888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297ce258193190bc937b47393b7953b6bc27687f59bf2a80fd83b97020e5d355`  
		Last Modified: Wed, 15 Jan 2020 01:51:02 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
