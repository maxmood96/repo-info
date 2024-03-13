## `eclipse-temurin:8u402-b06-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:bdce408731f709f2c2f2f7f69be7727c7acd92d7545baab3747c9d1755250b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `eclipse-temurin:8u402-b06-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2340; amd64

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
