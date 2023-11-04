## `openjdk:22-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:178578b97de1a0d26d559e36d0fb30c5a17fbbfd54498a2ec36a276c294e2dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `openjdk:22-ea-jdk-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull openjdk@sha256:230ec591e9139f4d769dc6df09bdd0a56417bdec06ee32f2a10ffc132ef03fad
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 MB (307961187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8d2dbaa7075ffa84d6ab076b6c5e1858abc26a09a2b1dd2d9b35519bf0c5a2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 01:39:37 GMT
SHELL [cmd /s /c]
# Wed, 11 Oct 2023 03:54:23 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 11 Oct 2023 03:54:24 GMT
USER ContainerAdministrator
# Wed, 11 Oct 2023 03:54:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Oct 2023 03:54:36 GMT
USER ContainerUser
# Sat, 04 Nov 2023 00:23:12 GMT
ENV JAVA_VERSION=22-ea+22
# Sat, 04 Nov 2023 00:23:25 GMT
COPY dir:131ba55a4f69828daf982fed083f8056b19f849ec8de395e5ceacac28b5e0b44 in C:\openjdk-22 
# Sat, 04 Nov 2023 00:23:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 04 Nov 2023 00:23:42 GMT
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
	-	`sha256:53f7d94044a293783b6667a23790497e452737d17d7221e9fcf940fd19c4f9c6`  
		Last Modified: Wed, 11 Oct 2023 03:57:04 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9d706d8cea409c86409f061201a999c5fdfc900eeb9cd2c8d7c214bd462f3b`  
		Last Modified: Wed, 11 Oct 2023 03:57:04 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c93fa899ae2056b59330f20c6e4a27ec6737929f17b7fa5a275baca12f8b1eb`  
		Last Modified: Wed, 11 Oct 2023 03:57:04 GMT  
		Size: 70.3 KB (70294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f049fc80168b8466bfbf3fd6b202ac8273bc9bd873e579290c2df3cb795a69b`  
		Last Modified: Wed, 11 Oct 2023 03:57:02 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb88ef9bb563e3c00ecbdc7e0d7b3cf42b300e6552b64a479d6feed9012aebfe`  
		Last Modified: Sat, 04 Nov 2023 00:25:44 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4c1b6c4c6d881bbd1565400ca3abfd867c50ad54f60306bea3c412221ddbcf`  
		Last Modified: Sat, 04 Nov 2023 00:26:01 GMT  
		Size: 199.6 MB (199578008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2528117806fec7f9a25447fc40c076f312235e3e3adb96b13363f028094a5a3e`  
		Last Modified: Sat, 04 Nov 2023 00:25:45 GMT  
		Size: 3.8 MB (3841778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7712b6171b44b80637b151952d4ce1b1c82acf3f01391861b65212fac30ae8f0`  
		Last Modified: Sat, 04 Nov 2023 00:25:44 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
