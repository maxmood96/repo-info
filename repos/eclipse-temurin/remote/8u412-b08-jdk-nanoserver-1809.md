## `eclipse-temurin:8u412-b08-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:a67c922fd1d00fc39111c083ff71ff9402a17da93f805a6d04c8b5e29545af48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:8u412-b08-jdk-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:43de2be4b109ce916e5817d2fbf91cd238a815fdce4d10aeac69f4a082ddf9d0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206734788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c412e835cff49c5148547874b6c60066201ab89a9b551f3bad16873108660b9b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 18:30:04 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 24 Apr 2024 18:30:05 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 24 Apr 2024 18:30:06 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 18:30:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 18:30:26 GMT
USER ContainerUser
# Wed, 24 Apr 2024 18:30:45 GMT
COPY dir:5498972beafb1de3e4749bc87b064f8ce9cec472aae9e7d0f4643a99f48638da in C:\openjdk-8 
# Wed, 24 Apr 2024 18:31:02 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:6c1aba89d9ebacd4f1369cd48d26d09c1a19c37a1bb267bca108af48fc1aab5a`  
		Last Modified: Wed, 24 Apr 2024 19:33:30 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66a02d1909bba7585a63ed513f0c7c5bbd6364e3a52b3b363b25890a8bfa166`  
		Last Modified: Wed, 24 Apr 2024 19:33:30 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e870db953193353980429b04bed7cc708680f15d0c432e2aa6f6dda4ea88157`  
		Last Modified: Wed, 24 Apr 2024 19:33:28 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd079869a94c991c70a1182afbad7cc1fc3ab25e82ead25390f279108d4344cc`  
		Last Modified: Wed, 24 Apr 2024 19:33:28 GMT  
		Size: 65.8 KB (65774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ef74b03f97dccf54dafc9c09e7fef7c0f6b60eb15ed9450d9f147aaa750ae0`  
		Last Modified: Wed, 24 Apr 2024 19:33:28 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f9e4b9e4d95967e3af1dcf04dc7d6fc8b6bbc204b86880778ea4628a5cb80b`  
		Last Modified: Wed, 24 Apr 2024 19:33:39 GMT  
		Size: 101.7 MB (101696590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74d54a754bd7ea1bf423a7014a15e223b6ae396fabb5c8f8ce5700ece5baf95`  
		Last Modified: Wed, 24 Apr 2024 19:33:28 GMT  
		Size: 77.5 KB (77484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
