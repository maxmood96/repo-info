## `openjdk:27-ea-9-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:000c0db5f8cdef826975c90211dd37af13bfb03428a5bc82fb183026f8306ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `openjdk:27-ea-9-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:035fa17a1f0e238307c38e0f18a1d62ef52569ddee79ec5cda286292aa8b32d1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.9 MB (423865305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b99e3341f5a85f694dce78599d5aff3bbb7c3da5d01e6dff46991f66c75976d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 17 Feb 2026 20:08:39 GMT
SHELL [cmd /s /c]
# Tue, 17 Feb 2026 20:08:40 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 17 Feb 2026 20:08:41 GMT
USER ContainerAdministrator
# Tue, 17 Feb 2026 20:08:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 17 Feb 2026 20:08:52 GMT
USER ContainerUser
# Tue, 17 Feb 2026 20:08:52 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 20:09:11 GMT
COPY dir:625a2d1f532d621a6c743669def3255030013f9f8e2976a431958fd4473522f3 in C:\openjdk-27 
# Tue, 17 Feb 2026 20:09:19 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 17 Feb 2026 20:09:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fc17a1f469c0eadfd8cfd4f8bf797b03f6d52135851c82505c393c1d834e44`  
		Last Modified: Tue, 17 Feb 2026 20:09:26 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e19c21f86adbccaec2ff72c8705a7f19427f420102b44ce6b31585fdc56c9ba`  
		Last Modified: Tue, 17 Feb 2026 20:09:26 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be2f94be82e7abb1f548564d719a2f3062740c0473bf8002eff6828692773b`  
		Last Modified: Tue, 17 Feb 2026 20:09:25 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac1e6d509efe5bc5d81c61ffe5a0b7face26e7e5bec0b2059c88d2b9f880b4`  
		Last Modified: Tue, 17 Feb 2026 20:09:25 GMT  
		Size: 70.0 KB (69993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d926350d75e3be64410cc50621d39ed4a7082de0011128774b234de77d76c79`  
		Last Modified: Tue, 17 Feb 2026 20:09:24 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec133a471510a2c2362188575b4bd59237c76a0f7669839770f643c946db7915`  
		Last Modified: Tue, 17 Feb 2026 20:09:24 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f254aca52fb9ea7dcfd30e0f62b8d48906f285c741a3a5558df3ecb98366561`  
		Last Modified: Tue, 17 Feb 2026 20:09:40 GMT  
		Size: 224.4 MB (224433941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb526eaec58873a30a044ec5258fdc1e70ee2b75a99f1498b6da5d9674145e1f`  
		Last Modified: Tue, 17 Feb 2026 20:09:24 GMT  
		Size: 103.4 KB (103377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24cc521ef471fde413d6b7c107e498aec8a9a9a34e97f7b79bc412904fc15cd`  
		Last Modified: Tue, 17 Feb 2026 20:09:24 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
