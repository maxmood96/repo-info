## `eclipse-temurin:25_36-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a61e59c85ee56d0560632dde75aa92db39d9342dcb41e390abf904c3bd455d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:25_36-jre-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:8e56f6bf2d4dc77ef68526d0a3efc0a39005e6a6687af06c7d83befa85628b92
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252762356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378deff391f3f98eb9b64c0cbc74cb44b21fae87733a8cc3a7a49a098fdfb352`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 19:21:48 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:21:49 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 24 Oct 2025 19:21:50 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 24 Oct 2025 19:21:50 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:21:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:21:55 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:22:03 GMT
COPY dir:8aa8ce0e84e7e6f80be28438d765894541d9d2eadfccff43ebe7257923223c3b in C:\openjdk-25 
# Fri, 24 Oct 2025 19:22:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3862129f466bcd484bbe660f09a2d8d34e05bdcdfc2a5d7f9f041703282b05b`  
		Last Modified: Fri, 24 Oct 2025 19:23:04 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb09cf02ef32375ff328c647a7d031fab7e60d4a4f3e8bce4e06d6ac39814a9`  
		Last Modified: Fri, 24 Oct 2025 19:23:04 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f636a7c7a12fa10b84d83fbaca3b446c077baef00c265360bed8e8c60531ee5`  
		Last Modified: Fri, 24 Oct 2025 19:23:04 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdbee1985614347a7a9d26ed8557f856aa701f970a533cff4459cc6001b74fd`  
		Last Modified: Fri, 24 Oct 2025 19:23:04 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1143a34bbed4a9cfb04812b29ac803668534817c0cbd7e217c220ee4f22360b`  
		Last Modified: Fri, 24 Oct 2025 19:23:04 GMT  
		Size: 70.2 KB (70171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae30e531a2b3f96d86349e1ce47422da3d9d4e868500f4612d4140103dda91b`  
		Last Modified: Fri, 24 Oct 2025 19:23:04 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff51d55cb786ef6d0d9602db864fe671851d5c91a7f317e698af4711390f061`  
		Last Modified: Fri, 24 Oct 2025 19:23:10 GMT  
		Size: 58.6 MB (58551009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35137eadbb1dc39baf71a40d372d6adb9a1f88c2e6e9e6b5afd846e99584b7b8`  
		Last Modified: Fri, 24 Oct 2025 19:23:04 GMT  
		Size: 106.4 KB (106411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
