## `eclipse-temurin:8u382-b05-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8783aa3e3a6ed478baa9699ddcc8aece83e73a93ea5f22d995c172d38e5a1b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `eclipse-temurin:8u382-b05-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull eclipse-temurin@sha256:4a8288c826e8f58496981256b68d2743e4908482306486b14dc0cd31065fb3bb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222198271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c566b00c630fb295b9471bca51acc75e2508a340b2a6ca5e7533d04e5642b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Sep 2023 00:20:14 GMT
RUN Apply image 10.0.20348.1970
# Wed, 13 Sep 2023 03:28:54 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 03:28:54 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Wed, 13 Sep 2023 03:28:55 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Sep 2023 03:28:55 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 03:29:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 03:29:10 GMT
USER ContainerUser
# Wed, 13 Sep 2023 03:29:22 GMT
COPY dir:809f08e9d949f52aad6441d5338932efbf6208a06192d58db41d3e3c11ba3f9f in C:\openjdk-8 
# Wed, 13 Sep 2023 03:29:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:8f8cef0759210af9d01a2fb45d79956a2db738bbd3734b7244b17e14ad945cab`  
		Last Modified: Tue, 12 Sep 2023 18:47:39 GMT  
		Size: 120.6 MB (120567584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d67aef4c483590cefd40495efc212f13e4c62993e8036c20bb4e19bc8620508`  
		Last Modified: Wed, 13 Sep 2023 03:47:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43d2dd9d6bd96273f79aded4034d866a5bf308ff6fdb9a4fc77fc002f96629e`  
		Last Modified: Wed, 13 Sep 2023 03:47:03 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098bc84e66e639101cddcf25cf0d33716dd5a1541283c6d39575f9d0b266ca3d`  
		Last Modified: Wed, 13 Sep 2023 03:47:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4194e5a793aa87b0833fa13729c4e38fc062f7c7cdd646bb2edf6967bb74308f`  
		Last Modified: Wed, 13 Sep 2023 03:47:01 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4f85d1fba3b190c64bf3f6efeeb898e2f9e65e7b0f420a909e95e1f2e08a79`  
		Last Modified: Wed, 13 Sep 2023 03:47:01 GMT  
		Size: 79.4 KB (79399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9742f2dfe73293118e72bd931d6773912a26d06055e981f42f8d48120ce3dd00`  
		Last Modified: Wed, 13 Sep 2023 03:47:01 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cab55a8d3900b6744dbc55b4054c600c71bf2b951c43a51c98b53a21710b0b`  
		Last Modified: Wed, 13 Sep 2023 03:47:14 GMT  
		Size: 101.5 MB (101470114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37becbd91d78bde7e45e79bbea3f4924612eae87a9858b8c9b3d54d4a6146f59`  
		Last Modified: Wed, 13 Sep 2023 03:47:01 GMT  
		Size: 76.0 KB (75951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
