## `eclipse-temurin:22-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:3e27c7429ee85b3c4f518a8a0df7c29f9c4fda19a39c74222020049bdb1d107b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:22-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:06ad3524dae97b7751028f25053d74f0c886e25f19fbd2ad8b25bab26cdf838a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308843511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466a7073da0bdf4817bf1675e54da00b6d131247d773291af1b6635394719f6f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:16:44 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 24 Apr 2024 19:16:45 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 24 Apr 2024 19:16:45 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:16:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:16:56 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:17:12 GMT
COPY dir:b848142647370c7b57f8798114952350d05bf467cc96eb22cf5219409c8a4580 in C:\openjdk-22 
# Wed, 24 Apr 2024 19:17:27 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Apr 2024 19:17:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99162cf301795a2934b58cb175b4b9bd833ba4ef022bdf311a3f5b6d4253f33`  
		Last Modified: Wed, 24 Apr 2024 19:44:34 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e333a85e4f99df6b7264ead3c9f8fc3447fc23c4a3283ca9a48b984c2213ed`  
		Last Modified: Wed, 24 Apr 2024 19:44:34 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92c1295a14273c026102afacdde9b5d3af241cc9b1e82084b9123fd995bf59b`  
		Last Modified: Wed, 24 Apr 2024 19:44:33 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cecf7884caa59b9e435973a173d2f68fcc934dc652a84735cd11fe9c51e8ed`  
		Last Modified: Wed, 24 Apr 2024 19:44:32 GMT  
		Size: 64.1 KB (64142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04fdbc0e3b8be01e12d59ba00b6ec0dcf8b86b227d058381f045173a941252b`  
		Last Modified: Wed, 24 Apr 2024 19:44:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41b6c6d34b427c27a266da6a150fae1ae147f862de4cdaa907b0da8e6a3949f`  
		Last Modified: Wed, 24 Apr 2024 19:44:52 GMT  
		Size: 200.1 MB (200052335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a649737477d156bbba1a6d80529c989ed753e0211a1aabb4d276f7aea6ce2def`  
		Last Modified: Wed, 24 Apr 2024 19:44:33 GMT  
		Size: 3.8 MB (3831613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba24ae4210af3f824fa354b18259fdd0cddc834cddb05e28f325dba00e06465`  
		Last Modified: Wed, 24 Apr 2024 19:44:32 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
