## `eclipse-temurin:22-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3aa24b0f21cc5516ad362c80e7d0c79ca3a72e4bdfb3918dee052132e5c3d8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:22-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:86230e67599b2ce315624e6c0d0bd696dfca025a52421cf49384fcd521c581db
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321197405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3da484d25116df4b4b9f5d697f4b238a172e17cbdf28b602a2b9b2cf1a2493`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:28:21 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 24 Apr 2024 19:28:22 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 24 Apr 2024 19:28:22 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:28:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:28:34 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:28:49 GMT
COPY dir:b848142647370c7b57f8798114952350d05bf467cc96eb22cf5219409c8a4580 in C:\openjdk-22 
# Wed, 24 Apr 2024 19:29:05 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Apr 2024 19:29:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54e00206cef5e76da3486dde342f4a50eb01cc49b8c1042b7701342348b7255`  
		Last Modified: Wed, 24 Apr 2024 19:49:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acdffbb40e6de7011c4567368181f7e153429174910a93038c555799fbdc511`  
		Last Modified: Wed, 24 Apr 2024 19:49:11 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d38fce880c0326fcf2b6af9ae5e85d7a617eaf1ffe97825619c4caf9bed4de`  
		Last Modified: Wed, 24 Apr 2024 19:49:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4131893637a6e4817646c84b0cf0afc69b50df6c8b33a5e8070696e2335855`  
		Last Modified: Wed, 24 Apr 2024 19:49:09 GMT  
		Size: 79.9 KB (79911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb232994dc1be2b521d2770debb36a482c6c3833f2201fc1ed14434e306e8d0`  
		Last Modified: Wed, 24 Apr 2024 19:49:09 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9824e2cd0a54d1300c9dfb893ca528c980782b41cb3215564ff0faee289f354a`  
		Last Modified: Wed, 24 Apr 2024 19:49:29 GMT  
		Size: 200.1 MB (200055536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258fa9fe72826a4143a2adda83e8f87fc5f1aad8249f83816c7bf84dce2ab6e3`  
		Last Modified: Wed, 24 Apr 2024 19:49:09 GMT  
		Size: 61.4 KB (61374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7dffb72ee055cf60fc36ef742a13ca3d0b6fad9263ec70b9e7ecbcf8082998`  
		Last Modified: Wed, 24 Apr 2024 19:49:10 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
