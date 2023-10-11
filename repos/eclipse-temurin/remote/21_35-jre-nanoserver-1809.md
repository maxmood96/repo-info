## `eclipse-temurin:21_35-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e8f25649e18d78f04b3338f103b64384a2562505768d6137e6591122f4fd9854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `eclipse-temurin:21_35-jre-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull eclipse-temurin@sha256:e32126c1995412e497a0760588f78398760d0f72fe9746389cd0494f604a19c6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156587283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40a68f72c2ef9d13f9831c5d7371ca3c1c0b7a0da75fd6641eca039c71a518`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 11 Oct 2023 17:42:18 GMT
COPY dir:5d7e2a5825eef6d21094c71010e496d2276d2a39ff1ed82cc9374a1e7bd17e0b in C:\openjdk-21 
# Wed, 11 Oct 2023 17:42:29 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:6ec9c0070349cf9c3e7c7090774e05c18266afc8641e54ea363ba812f5c7d6c9`  
		Last Modified: Wed, 11 Oct 2023 17:49:40 GMT  
		Size: 48.7 MB (48687908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1b3f622efc1b91d61236baa3776906c5ab6eb73f9756cc57987d1094ddda04`  
		Last Modified: Wed, 11 Oct 2023 17:49:32 GMT  
		Size: 3.4 MB (3361090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
