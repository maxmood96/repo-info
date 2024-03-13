## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f704a2d64078293934ad97d1c5360c17aadeafeaab4ec2dcc741a189a6e8fa10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull eclipse-temurin@sha256:8a42f23bc839897dc2dfcd208fe4395b1e3de9768670c30c14f407e7e41ecdc8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144895861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cfb67f8c257f548e709ee8ddd7f52dc342153c69571120493dfb60032695b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 00:41:38 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 00:41:38 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 13 Mar 2024 00:41:39 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Mar 2024 00:41:40 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 00:41:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 00:41:51 GMT
USER ContainerUser
# Wed, 13 Mar 2024 00:46:59 GMT
COPY dir:db8ed4bc6cf3fc1a9a530d737bd8bcda792821f4f1e3e610cedaee77629ebb36 in C:\openjdk-8 
# Wed, 13 Mar 2024 00:47:10 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9569a24b1d9b596a48436098ac5fe49c52e3153cd3bd147e365a80a4059570fd`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ac6979d3018020e5d56f24192e72d677112ce70959b875a73d0ceb74f7ab4a`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a09b00f17d16e8707c45a7f82c7b23111fc4386bb12c142f745c8f3d75630a0`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d598c02e10beef0b23187e3090a387054f0aaba86c9b427e0e59a2b6cf0375cf`  
		Last Modified: Wed, 13 Mar 2024 01:31:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df21f9058d8a1bfd11006bb0255f88c7865c2c34851a191447c198e670ea384b`  
		Last Modified: Wed, 13 Mar 2024 01:31:05 GMT  
		Size: 68.9 KB (68906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8255b1c5b4f751fb254a0543c26a87c06339f37b1f99fb38054529a1941b9`  
		Last Modified: Wed, 13 Mar 2024 01:31:05 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7327bdcb6663c24af50cfde472b143643988b08f2345da772b271e816de1fb6a`  
		Last Modified: Wed, 13 Mar 2024 01:32:16 GMT  
		Size: 40.1 MB (40113792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d128228ab37d6998c19ff029665fcbe6bca33a86420330277672b2907b6521`  
		Last Modified: Wed, 13 Mar 2024 01:32:10 GMT  
		Size: 87.3 KB (87260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
