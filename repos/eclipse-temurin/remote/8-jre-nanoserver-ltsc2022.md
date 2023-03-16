## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7e94574a7a3049f214da00238a09b7c2a0a80198e7d766f4150f2891874dfb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull eclipse-temurin@sha256:a6b568ffe8e02971266d1d306a5a2d30351c284a255ffe62f841b864dcebd91c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162274505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b014feeff281f74e524c0a673b342bb9bd27898e1add3216749a2f423dbec1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 Mar 2023 06:31:34 GMT
RUN Apply image 10.0.20348.1607
# Thu, 16 Mar 2023 01:29:33 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 01:29:34 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 16 Mar 2023 01:29:35 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 16 Mar 2023 01:29:36 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 01:29:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 01:29:55 GMT
USER ContainerUser
# Thu, 16 Mar 2023 01:31:07 GMT
COPY dir:dcd2674e91fb412db18990a7004f7a484148b702bd6de08f5ae3a3d6f6a3f6f8 in C:\openjdk-8 
# Thu, 16 Mar 2023 01:31:26 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:7abf0a70d48bf65f3d985f5780d4bdaece36f1f4bb8be10d5a6aacce33dacc75`  
		Last Modified: Thu, 16 Mar 2023 01:54:24 GMT  
		Size: 122.2 MB (122171731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a611a20686e9374e3a55a49399506f83c041ae711ed47018c2267c341156dd97`  
		Last Modified: Thu, 16 Mar 2023 01:53:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4d6464959d95eab200c9a49617a9855ec77e0de5a20563e87c1a56e8c25f4`  
		Last Modified: Thu, 16 Mar 2023 01:53:50 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29dfedf32262d5595636120ea0904b9230ad36710eb1b92ec3fc339f2f8f732`  
		Last Modified: Thu, 16 Mar 2023 01:53:50 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c7189a4a615fd7df46d6561fae78a2d4fd0868a85a3d6ba60d2b9f9a5cc633`  
		Last Modified: Thu, 16 Mar 2023 01:53:48 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bd03bc0018decd48fb94c93ab94e095a0a872bc5d358e40f4b3733d7bd517f`  
		Last Modified: Thu, 16 Mar 2023 01:53:48 GMT  
		Size: 90.1 KB (90142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a09b5f72b3f9a8e103254e56666bfefa259756235941f52d69d96d1ad2cc03`  
		Last Modified: Thu, 16 Mar 2023 01:53:48 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9665a22e7206ecdfd56259b5334854517a782c022a959d5866940225321b31f5`  
		Last Modified: Thu, 16 Mar 2023 01:54:44 GMT  
		Size: 39.9 MB (39934203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beeffb4435de70256a4390a40dcb402acce3f65f431c0081a894c2b543ac88ec`  
		Last Modified: Thu, 16 Mar 2023 01:54:36 GMT  
		Size: 72.6 KB (72631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
