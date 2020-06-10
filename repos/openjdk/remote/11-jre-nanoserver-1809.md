## `openjdk:11-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:9d93d9d149beed1c246a8c92f7acfe6b8ba0159f99c28572b7989c1620ace8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `openjdk:11-jre-nanoserver-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:289e5bcdb25344d2d86e2b19cde4feebd8b3ccc83d29ba7e5579332934d1269d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140289381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b081649dc8f91d86be89259508ba2fbbe5a09885ddd6748ac7112fb02f56c9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jun 2020 11:12:32 GMT
RUN Apply image 1809-amd64
# Tue, 09 Jun 2020 22:42:44 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2020 22:58:56 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 09 Jun 2020 22:58:57 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2020 22:59:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 09 Jun 2020 22:59:09 GMT
USER ContainerUser
# Tue, 09 Jun 2020 22:59:10 GMT
ENV JAVA_VERSION=11.0.7
# Tue, 09 Jun 2020 23:04:16 GMT
COPY dir:5079dca1201fb18611f476ef87596f1f7b8bce8e365c08f25921689ee5b44ccb in C:\openjdk-11 
# Tue, 09 Jun 2020 23:04:34 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version
```

-	Layers:
	-	`sha256:c7d6d47ff7dfb2aa4d4e819641b93ec971e8541978dff0ffc24c193babeb8c07`  
		Size: 101.0 MB (101043386 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5b390ee94e41353252b153770fa99d748992b90bdaf9abf7c785d93be52ee02c`  
		Last Modified: Tue, 09 Jun 2020 23:19:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9a662d48ac48ee274c609c486797c7cd8a0b56c6bc3b461883800eeaf2c5ec`  
		Last Modified: Tue, 09 Jun 2020 23:29:52 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650227bb8b4a8da580189fdfe9b85d0709e6a9ea2f5bfe62a44bb433d38f0c6f`  
		Last Modified: Tue, 09 Jun 2020 23:29:52 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b231c56c00e2a9eac7e47b38dffd0de11c5d952b4b891883fb0b90c5c03f80`  
		Last Modified: Tue, 09 Jun 2020 23:29:52 GMT  
		Size: 65.5 KB (65507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0f9eacbfc9a371e4b683bc634dda259ae0235eb4ad70ede1769461086bf13c`  
		Last Modified: Tue, 09 Jun 2020 23:29:50 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e841e65606242dbd8001653782ebcee54a65b69123c30e5cb3d74281e81cb2c`  
		Last Modified: Tue, 09 Jun 2020 23:29:50 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a04f49fd8c8ba0e7c781a27104a318e30a7b49eafa9e22b92b4d7a8fbb096d`  
		Last Modified: Tue, 09 Jun 2020 23:32:19 GMT  
		Size: 39.1 MB (39121519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf255517815c2a057736d867036d1eb8f02ded6e2ec666266e982fec773d5fde`  
		Last Modified: Tue, 09 Jun 2020 23:32:11 GMT  
		Size: 54.5 KB (54519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
