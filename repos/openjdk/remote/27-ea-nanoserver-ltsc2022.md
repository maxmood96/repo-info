## `openjdk:27-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:6710a6abf016d409262dc5f5a2c1fb720f93a7e3f8aa8994cf70229164c5ed40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `openjdk:27-ea-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:22fc44168735992830cd554eb063bab8059e4b11215c971fc915c0d00bc859e1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347284976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397024f452aba2a13314b7a100bb975934de94310653973d7a30d839e2d040f8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 22 Jun 2026 23:09:35 GMT
SHELL [cmd /s /c]
# Mon, 22 Jun 2026 23:09:35 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 22 Jun 2026 23:09:35 GMT
USER ContainerAdministrator
# Mon, 22 Jun 2026 23:09:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 22 Jun 2026 23:09:48 GMT
USER ContainerUser
# Mon, 22 Jun 2026 23:09:48 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 23:10:19 GMT
COPY dir:0d582b259e10424ad2a400d25138b5e85d8dcedb2869ba13c9537e008882334c in C:\openjdk-27 
# Mon, 22 Jun 2026 23:10:25 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 22 Jun 2026 23:10:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839550b1ca6a1dd3edc9a8b28ada9b4b42a819510511d5c1c4c91d8bfb14fb54`  
		Last Modified: Mon, 22 Jun 2026 23:10:32 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24646209cdf17d43a16599196bee3fca0d73f6c9a93961c635f13f012d9bbbb1`  
		Last Modified: Mon, 22 Jun 2026 23:10:31 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf7934396040d8fdf70e9d00b6ad67564ba80cdf30fc96026619db536f63401`  
		Last Modified: Mon, 22 Jun 2026 23:10:31 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c179a9fdf4f3b95d6eb8a57d8cfc5548788168341f614535759d4abe626aefb0`  
		Last Modified: Mon, 22 Jun 2026 23:10:31 GMT  
		Size: 85.7 KB (85681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba683788f15bf73b12f8c23a322b6299ea8f483b4a50ee541aa643459e80b833`  
		Last Modified: Mon, 22 Jun 2026 23:10:29 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52057151fbdef61ab9f0e837f6d9c752313f96cf88ca4f66cd51f838b8deb36`  
		Last Modified: Mon, 22 Jun 2026 23:10:29 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311050faa3a014a9d49eb56811b4385ad3168d3405e0028d807469a2d24638ce`  
		Last Modified: Mon, 22 Jun 2026 23:10:44 GMT  
		Size: 223.1 MB (223101070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6047afc6d76c795e7fa8ac6e49e410b569e2f394670c77d2fa777b9f4e6f914d`  
		Last Modified: Mon, 22 Jun 2026 23:10:29 GMT  
		Size: 94.3 KB (94334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34eecb679aaa37080885ae54f2e9530ed3f6beac1d577c100f0b1d472c72bbb`  
		Last Modified: Mon, 22 Jun 2026 23:10:29 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
