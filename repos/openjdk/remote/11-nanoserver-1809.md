## `openjdk:11-nanoserver-1809`

```console
$ docker pull openjdk@sha256:a52a54738c358623799bcb0235b7484c87680ade848593ee0cdf9d0803be81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `openjdk:11-nanoserver-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull openjdk@sha256:5ad91b77681101a84c28618066161c05310f29e6b8b47cbe214e65069b9d6f7a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291145715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35112462e728c7f71cc3ef89405fb5d9dd11d819c0d586901d07fac1cab7dcd3`
-	Default Command: `["jshell"]`
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
# Tue, 09 Jun 2020 22:59:57 GMT
COPY dir:d90d60e1c0505496926373a51cab7b6b2c4fc0bb30d14b79fe3ef70ac0ba6a6a in C:\openjdk-11 
# Tue, 09 Jun 2020 23:00:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Tue, 09 Jun 2020 23:00:33 GMT
CMD ["jshell"]
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
	-	`sha256:881760a8c4206b6e3f2e48362ed3af1531f02b6bdde2470f17d000e092170da3`  
		Last Modified: Tue, 09 Jun 2020 23:30:09 GMT  
		Size: 190.0 MB (189976118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06a51b6462ff888f05637a0f6a1e2d7e854422387409956083c9b03d47bb534`  
		Last Modified: Tue, 09 Jun 2020 23:29:50 GMT  
		Size: 55.3 KB (55336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf94b7058baca78c270f8dddbce455323dfde475530f297b512ca83d113cb13`  
		Last Modified: Tue, 09 Jun 2020 23:29:50 GMT  
		Size: 918.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
