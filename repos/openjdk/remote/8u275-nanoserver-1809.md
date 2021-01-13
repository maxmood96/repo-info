## `openjdk:8u275-nanoserver-1809`

```console
$ docker pull openjdk@sha256:f7311af50f3bf8fa3f383d6316ecbfd123eee0b51638785fae4444b940dbfd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:8u275-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:62aa1629d621685764086017ca9d11f1d9a13e07cb03f509fdef7d1e97fe7e32
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202472062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ff9839074beb2e4c520ab622fc616b4918722148ef040ee5ac6166aeb4da49`
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
# Wed, 13 Jan 2021 21:02:31 GMT
COPY dir:0892804dd065b22adc43ce2caaaf5966043723850b9894e42783006f86478881 in C:\openjdk-8 
# Wed, 13 Jan 2021 21:02:51 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version
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
	-	`sha256:8e8f7ed36684556a51b746aba245408b37234ad7846b17ddbd208cd04367333e`  
		Last Modified: Wed, 13 Jan 2021 21:40:57 GMT  
		Size: 101.0 MB (100972643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2087a5628a4b82d2a73349cc7f64590fc5fe3289ba08250eb034ce754148d9`  
		Last Modified: Wed, 13 Jan 2021 21:40:45 GMT  
		Size: 90.1 KB (90051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
