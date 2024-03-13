## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6da3d63df14f5cc6c24901152fd3dbd31d0670cfa69d159710146d615fc8d6f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.2340; amd64

```console
$ docker pull eclipse-temurin@sha256:46edc7d2342672c4a4af39a5e83aea0287b3acabfd9213ee6c833304cfb48311
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160975537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add89527ca439a27bc453b8b77d1447a266c2c2e2d488b43150109f65404f18a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 01:20:55 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 01:20:55 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 13 Mar 2024 01:20:56 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Mar 2024 01:20:57 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 01:21:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 01:21:11 GMT
USER ContainerUser
# Wed, 13 Mar 2024 01:21:52 GMT
COPY dir:db8ed4bc6cf3fc1a9a530d737bd8bcda792821f4f1e3e610cedaee77629ebb36 in C:\openjdk-8 
# Wed, 13 Mar 2024 01:22:04 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e98336f720b829e374bd1d59306210d3700861b11d3df51506afbc0b50d039`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c079b182eda7b2ab08c47e780f59a7b77e54541a35de305d05927577035b30b9`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6059e0fbeac8935bc15cc89e2b57e005314533c61cf3d4276b5e731fd46fef35`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8070e272015e9632bdda4cd151f601deeeb4345fcf61701d5133689cca3ed6`  
		Last Modified: Wed, 13 Mar 2024 01:40:24 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21dba345c47f39abd739524299d8d68413c670c39bccce29ba922fd4e548e735`  
		Last Modified: Wed, 13 Mar 2024 01:40:24 GMT  
		Size: 84.0 KB (83968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a06064b35b70fc8c4f626eb883a0d291ba26423f241de3f0ddb0f7cd83641`  
		Last Modified: Wed, 13 Mar 2024 01:40:24 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086230b2697dfc381325d26dd7c6e05aa48721d1885cd8801c0c99478c5fae64`  
		Last Modified: Wed, 13 Mar 2024 01:41:04 GMT  
		Size: 40.1 MB (40120751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6c63c606d221d9fd051b09c2b59e1d7b566a1c89dfcbc94d1601bb1af4201c`  
		Last Modified: Wed, 13 Mar 2024 01:40:58 GMT  
		Size: 62.3 KB (62298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.5576; amd64

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
