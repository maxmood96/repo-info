## `openjdk:8u275-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:dd0d04a064a179616b74aab61add7690e0f0379241545b50084594515220ac5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:8u275-jre-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:849389684b9ab2e326e1af7908688c0e79e5ca0870a86bf6a464533c494be85e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139680728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c83888d8852f90675995508278ec7ffcc81b3bb74fbbdaf511d8a4068bb3d92`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 21:01:53 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Jan 2021 21:01:54 GMT
USER ContainerAdministrator
# Wed, 13 Jan 2021 21:02:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 13 Jan 2021 21:02:06 GMT
USER ContainerUser
# Wed, 13 Jan 2021 21:02:07 GMT
ENV JAVA_VERSION=8u275
# Wed, 13 Jan 2021 21:05:59 GMT
COPY dir:9c574feda3d434860f596ed9945da2b2916773d80cfb9282fa700c98a8998c43 in C:\openjdk-8 
# Wed, 13 Jan 2021 21:06:15 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2b6c001c337f812bceb3b03d15a70d1d9905540658e751e42f20f7cc0ddc819`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb6e28c3ff306f6c33045aed2e65fcab8f045964fdf585fd9ff1a04fb6f4f1`  
		Last Modified: Wed, 13 Jan 2021 21:40:49 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9732ca3e0c38e5c843b184efac598a5a240580f63845fd6d6785d74beb864c5a`  
		Last Modified: Wed, 13 Jan 2021 21:40:48 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f226704d058e27f81a0b344cc0c09c4c8e2604ae02105ee61981cec67ee74c`  
		Last Modified: Wed, 13 Jan 2021 21:40:46 GMT  
		Size: 64.9 KB (64879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba37b590809af3c8a52b218cd2c383b7017b5628bcba2e0290e0d379dc2404c`  
		Last Modified: Wed, 13 Jan 2021 21:40:45 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83556138e5e33052e04fc0c4ca5ada197920308b05d44e1bd581fa77f14e050`  
		Last Modified: Wed, 13 Jan 2021 21:40:46 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c289dec2399aca3aa9e53e94a9388ac8abf1e373b4fa056977ccc5975ad97a`  
		Last Modified: Wed, 13 Jan 2021 21:42:11 GMT  
		Size: 38.2 MB (38191127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aa40c55520792423fe8feeba8aca140cafea182ee87578b2d012bfdd481ee7`  
		Last Modified: Wed, 13 Jan 2021 21:42:05 GMT  
		Size: 80.2 KB (80233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
