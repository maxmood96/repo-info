## `eclipse-temurin:8u382-b05-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ad8a69f8e358580f60b07087e7b1e4685b5a8d8438ed3753e6dffeb86941357f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `eclipse-temurin:8u382-b05-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull eclipse-temurin@sha256:6237d78a28473e9db2914f8f79c684405caa717eb3615d2d8add3b49011eb779
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160695325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2467dbd6cf9fe78bcdd36fa7e11b277f7bbd2d0b2e6583c1a81edb2fc2628935`
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
# Wed, 13 Sep 2023 03:29:51 GMT
COPY dir:f24575d0fd9e2979f5a8010c202ec6d963a3eb3cd788517e3ab1d758c8e6ad81 in C:\openjdk-8 
# Wed, 13 Sep 2023 03:29:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:7000541ffd9ff9b9083c292c2c0c6bdc47a1c39c0eaff1535229900f58365240`  
		Last Modified: Wed, 13 Sep 2023 03:47:32 GMT  
		Size: 40.0 MB (39981176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d200a956a697b17ba6976a288ae637e886c42f57a6251aff0b10994cd479a4be`  
		Last Modified: Wed, 13 Sep 2023 03:47:25 GMT  
		Size: 61.9 KB (61943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
