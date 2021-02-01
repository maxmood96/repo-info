## `openjdk:8u282-jre-nanoserver`

```console
$ docker pull openjdk@sha256:8dad6868ae723360c28844c95c79ae2ab5b3c0aa08dcea6abf677a964eddab1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:8u282-jre-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:0a7db4af6fe3789073c9e063177a37f016ab4ddcb660e25d32feea6068c54287
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139700818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7001c60dff65d9c62a1bac6e553b9ad97b9dfc2273cd61a8cf4c38ae14f5db29`
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
# Mon, 01 Feb 2021 19:46:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 01 Feb 2021 19:46:26 GMT
USER ContainerUser
# Mon, 01 Feb 2021 19:46:27 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:49:13 GMT
COPY dir:f51b6315789fea62bc81073100310d85cf4082234fc7f3bd9b51f6f4a883a8f3 in C:\openjdk-8 
# Mon, 01 Feb 2021 19:49:21 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
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
	-	`sha256:7a8a1838c8bffd2a653ab062f96dbe30c5f8dc4bddf58a06cabd73f76640cec5`  
		Last Modified: Mon, 01 Feb 2021 20:09:42 GMT  
		Size: 67.8 KB (67811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac4dfc6af685bd979e4f8c7d8d73bf0a2fb5a0c7e8a0d4ed8865c6a58f92d16`  
		Last Modified: Mon, 01 Feb 2021 20:09:42 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3503f37a486e59dbcbf5305a66eacd9c35d40e7e84733fb6538d6c362325f251`  
		Last Modified: Mon, 01 Feb 2021 20:09:42 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a557e3457e6d67e4f1884aa5e54766262dbe604715363e93f6cebfd1e6ac6d`  
		Last Modified: Mon, 01 Feb 2021 20:11:05 GMT  
		Size: 38.2 MB (38198634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107aec69f7c37d44eca0f70f5e79668593ba26dd9d4bf31c8770e47b0becd613`  
		Last Modified: Mon, 01 Feb 2021 20:10:58 GMT  
		Size: 89.3 KB (89307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
