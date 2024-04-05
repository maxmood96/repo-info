## `openjdk:23-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:9eab7b75e6e934301c176de220ae93c266841cd6645eb7c4575b8b8502582031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-jdk-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:a6e718791f7925c3b25e48ab455042afabcbf778dfb2ebb446f905b1ee4dd89a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315412151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc470332c03c1e6080ce062368e5daff5305b1383b2cce49a640b1adfe26c4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Fri, 05 Apr 2024 18:51:52 GMT
SHELL [cmd /s /c]
# Fri, 05 Apr 2024 18:51:54 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 05 Apr 2024 18:51:55 GMT
USER ContainerAdministrator
# Fri, 05 Apr 2024 18:52:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 05 Apr 2024 18:52:05 GMT
USER ContainerUser
# Fri, 05 Apr 2024 18:52:05 GMT
ENV JAVA_VERSION=23-ea+17
# Fri, 05 Apr 2024 18:52:15 GMT
COPY dir:5167fe4891c14c331f4ba4ef8d2f5decc066863be20ac52b35dd14a9c2c8a27a in C:\openjdk-23 
# Fri, 05 Apr 2024 18:52:27 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 05 Apr 2024 18:52:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2feec2601def3def94f93aab8da0ceaba78f7b7b4b0067469b56300e0ebf607`  
		Last Modified: Fri, 05 Apr 2024 18:52:33 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d984f8d1c6a2b080c61e4193d93910d1df1d7f552a5ff1d9cd4897c42b36af7`  
		Last Modified: Fri, 05 Apr 2024 18:52:32 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e21e41f027dfe3098f9b214c1221315e4994b03397d7ff90f1a9b45cf634835`  
		Last Modified: Fri, 05 Apr 2024 18:52:32 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c396d2d41b1ef8306aaf6cdb9e8965bb35153c43df7d04c3453f3c306d51ce37`  
		Last Modified: Fri, 05 Apr 2024 18:52:32 GMT  
		Size: 68.7 KB (68704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ee593b4b134a221f48cd5de7d0336c07355cadbccdc95fe796ba82f9973101`  
		Last Modified: Fri, 05 Apr 2024 18:52:31 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c582442a4f0d02a37eef362ffd990ace18ec5a66d359181d34b6c6eb7d8eed`  
		Last Modified: Fri, 05 Apr 2024 18:52:31 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3649a5754f813ae9f1c210fe662c05ea22576833375a71e4d84836fdd54a5caa`  
		Last Modified: Fri, 05 Apr 2024 18:52:42 GMT  
		Size: 205.3 MB (205283599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2f41a59661528bdfc12facf2c5852471a6263fb1a7f41d77ff0f8cd3409ce7`  
		Last Modified: Fri, 05 Apr 2024 18:52:32 GMT  
		Size: 5.4 MB (5433513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bde03ba5519c323c7f33bcab9e0556f7035e72c611a905f6e96d91e2cb7966`  
		Last Modified: Fri, 05 Apr 2024 18:52:31 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
