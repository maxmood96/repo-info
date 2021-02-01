## `openjdk:8-nanoserver`

```console
$ docker pull openjdk@sha256:337768d2d6ba933297bd71f1cac9493b27828f3cdd5b4d8aa98bb1fa8fc0f4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:8-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:6cd07fa595e357f08f91a2e0eaf9feeac828537ce95da879f17b4a8285940d90
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202493703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d32dcbf4fffcd37bc55fab3128a584d1817659c37a7fc9d53faf3d9b1d2830`
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
# Mon, 01 Feb 2021 19:46:38 GMT
COPY dir:6f6bc9ea1f93ff1db59b5fd63225d3a5b1df7d373dee2c520410df56c408f0e1 in C:\openjdk-8 
# Mon, 01 Feb 2021 19:46:48 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
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
	-	`sha256:ee3041ee5c75ba33349edea2bc3c41429b267ff4d935dab2c9ff8a0f6d1e18b7`  
		Last Modified: Mon, 01 Feb 2021 20:09:54 GMT  
		Size: 101.0 MB (100989482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd727bcf6fbc37eb6c70548340273ae45010514eef8d4ef25217c35b9d36a88a`  
		Last Modified: Mon, 01 Feb 2021 20:09:42 GMT  
		Size: 91.3 KB (91344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
