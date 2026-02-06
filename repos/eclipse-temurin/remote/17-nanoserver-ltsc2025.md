## `eclipse-temurin:17-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d9d03b51051df217f45a32aa704e2ef82837fe1d2abeed6f56cac39cf9529c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:17-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:c697940987ad8b2857be2062b9d2f6886012b8f335d000c52d3439bdeb33d0ab
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386748988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6a5c852b77e52eb7237d98d1608a75a09b918cd7c98b7ac207889ad5a3c94e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:39:59 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:59 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:39:59 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 05 Feb 2026 22:40:00 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:40:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:40:05 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:40:27 GMT
COPY dir:fb23a79434a3e7defa51a1bec1a7ef896ff849f7ba85f2629e1913957db57a2e in C:\openjdk-17 
# Thu, 05 Feb 2026 22:40:31 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 05 Feb 2026 22:40:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c28ad352328c336e71b349a7e2bf7470260cf46fe57b84f51af49bb5af7086c`  
		Last Modified: Thu, 05 Feb 2026 22:40:37 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c56825c524ba6696eb33ad58e3662e6b4a2b0da8ca625cfa5c76a3b6251e7c`  
		Last Modified: Thu, 05 Feb 2026 22:40:37 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99846abca5b7f14b5b8cab545c4f0f310095254613ca4c14e4cd5285856b3921`  
		Last Modified: Thu, 05 Feb 2026 22:40:37 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7052286fe390d44664616fe4d5715d375253a283f0b115ba6437a7505d47e10`  
		Last Modified: Thu, 05 Feb 2026 22:40:37 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c5441d14dba5ac322e920d3cdbf11335281b83071d6b535a014756968c8db5`  
		Last Modified: Thu, 05 Feb 2026 22:40:36 GMT  
		Size: 76.6 KB (76629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96a008514f338791b007cd2663dca1adaa733fe7774c3ca272ab7959398000c`  
		Last Modified: Thu, 05 Feb 2026 22:40:36 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00e14e8edf3ab9fdf469872960ff5be8cd1e0593e481e77861644a7611cccc2`  
		Last Modified: Thu, 05 Feb 2026 22:40:48 GMT  
		Size: 187.5 MB (187486644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75eb7825b2f256704b774abf1660575ccb6cdfcf6c1e2927f0ad76ef243fd1d`  
		Last Modified: Thu, 05 Feb 2026 22:40:36 GMT  
		Size: 102.8 KB (102760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d1a9177840eb32d159981e714cf1fc75fe94ea0a5dd1b689f8eeb1c86450e0`  
		Last Modified: Thu, 05 Feb 2026 22:40:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
