## `eclipse-temurin:21-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:87cfa00695beba981fc4e443335653862e963c974241202ab9d22f57d71a74d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `eclipse-temurin:21-jdk-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull eclipse-temurin@sha256:81a9b47a532d9c6624ea55506736d9c5248dca97a49a226cce03dea49f7b445e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308507382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a08652a3f95efacabf9e5bc1c3c09610b985d66fffa4c3bb53052abf7659acd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 01:39:37 GMT
SHELL [cmd /s /c]
# Wed, 11 Oct 2023 17:37:40 GMT
ENV JAVA_VERSION=jdk-21+35
# Wed, 11 Oct 2023 17:37:41 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 11 Oct 2023 17:37:41 GMT
USER ContainerAdministrator
# Wed, 11 Oct 2023 17:37:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Oct 2023 17:37:50 GMT
USER ContainerUser
# Wed, 11 Oct 2023 17:38:04 GMT
COPY dir:f06f5ee7db845501c8fe05855f9c29461cda8cefd674e3441d48367166fadd37 in C:\openjdk-21 
# Wed, 11 Oct 2023 17:38:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Oct 2023 17:38:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c11581d9ee9ea19d58c6cbb415dd809a51b56502169a7a5b301da76d79f63b`  
		Last Modified: Wed, 11 Oct 2023 03:57:05 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9398e98529623d763369e9e2c652d1da81a3703f5293d2fb641345db0b9457`  
		Last Modified: Wed, 11 Oct 2023 17:48:19 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb28d12582ac1a7f7f8fe9eeaebc7c156fbd708d933124aba3ce3e8d1094e530`  
		Last Modified: Wed, 11 Oct 2023 17:48:19 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6980ee689278b3d8868dd2c5caaf47cc79500e9d875d7b49997f0b3caf234e`  
		Last Modified: Wed, 11 Oct 2023 17:48:19 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6a2347c8237ba989350480d3e7a6e867e935c05894ce61fc61910d02ee3b5b`  
		Last Modified: Wed, 11 Oct 2023 17:48:17 GMT  
		Size: 67.9 KB (67906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7cb4e315edf3e55fd58ab6d67c2b7eaa79a7518ab53e8bc27e6a0338279d95`  
		Last Modified: Wed, 11 Oct 2023 17:48:17 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214fa640e07046e7f97ac8695e78e56dc8583800b580e51a6377ef1143a88c53`  
		Last Modified: Wed, 11 Oct 2023 17:48:38 GMT  
		Size: 200.2 MB (200157682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16b741117e2bcb99ff37c91ff4902c1a535b6bfd27c745c06b7667666caea2f`  
		Last Modified: Wed, 11 Oct 2023 17:48:18 GMT  
		Size: 3.8 MB (3810254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4fba254d312f3920237ce49bc619a28becdd43eb1d7cfeb2cd43bf2ffbc609`  
		Last Modified: Wed, 11 Oct 2023 17:48:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
