## `openjdk:16-nanoserver`

```console
$ docker pull openjdk@sha256:a9247ec85f173f14f40f84f4ccaca8a88f9e3e72065b2592768439ac30f05c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `openjdk:16-nanoserver` - windows version 10.0.17763.1577; amd64

```console
$ docker pull openjdk@sha256:2d1c0d0eed6994d96f2b6ccf89bf3f37de68779e41a8e5864b301aef9770cf77
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285007518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8712f840f9360e5e77f8724b28dbeffe66f47163409a5a76eca2d6bb2d9c6f12`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:53:16 GMT
SHELL [cmd /s /c]
# Wed, 11 Nov 2020 17:53:16 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 11 Nov 2020 17:53:17 GMT
USER ContainerAdministrator
# Wed, 11 Nov 2020 17:53:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Nov 2020 17:53:32 GMT
USER ContainerUser
# Thu, 03 Dec 2020 22:18:39 GMT
ENV JAVA_VERSION=16-ea+27
# Thu, 03 Dec 2020 22:19:14 GMT
COPY dir:99f811290cbed9d3a18665555a2b1dd859a8c3fc4fc549c64898d26e30c1b13a in C:\openjdk-16 
# Thu, 03 Dec 2020 22:19:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 03 Dec 2020 22:19:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:41b7be9dc08821cf81d29b16e0df54f7f3e3aeaa6407f43520c6259f2d84b10c`  
		Last Modified: Wed, 11 Nov 2020 18:27:27 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e637122599038842d743045a8ebfbfa35dbadf7dfee0adcc2ba903e891ab072d`  
		Last Modified: Wed, 11 Nov 2020 18:27:25 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7fa5c85bf3c3dc79cf3bec9aba597aa0b5c38c234952da905e86d7a556b6f3`  
		Last Modified: Wed, 11 Nov 2020 18:27:25 GMT  
		Size: 912.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9c6b451f516c5e78ab16ded450d01a2a45dd13d0cac12cb9b043f5d87f993a`  
		Last Modified: Wed, 11 Nov 2020 18:27:25 GMT  
		Size: 67.3 KB (67302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac0f27f5ace77a66a18d26e72bf8f24216110f8ed5b6f951597b9a42d3ae52b`  
		Last Modified: Wed, 11 Nov 2020 18:27:22 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71518339c027deb23c57f03dab6a4fd8c9d61046aa8d2d6aad11b91ae3e85e39`  
		Last Modified: Thu, 03 Dec 2020 22:28:18 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b25dba14e29e43d417db1c8ba068b0ba4197960ad2362e1e41ce900bfaec7a`  
		Last Modified: Thu, 03 Dec 2020 22:28:36 GMT  
		Size: 180.0 MB (180017289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1282682f123d4470d2ddf60b84de04df6a03e296cb31b80b33b7e9f2d6f981d6`  
		Last Modified: Thu, 03 Dec 2020 22:28:19 GMT  
		Size: 3.6 MB (3638003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eae2065401f1f2d3172d567f5b1cd196a95e4ceff424f1665a885c8850ebe2b`  
		Last Modified: Thu, 03 Dec 2020 22:28:18 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
