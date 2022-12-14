## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:fce0d8d13d4526eb538e6a02b2f23131301c0a8f2fb449f8eb45be9ad5de3180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1366; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1366; amd64

```console
$ docker pull eclipse-temurin@sha256:01b70b67357f16f197f5933c99140fd57c81a80e9f566b8a4ad415c119e9bb52
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222743437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a15d4212924bca1b00092f08aa1b1947e67b563b52819582068ca18c9ff7f03`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Dec 2022 09:19:21 GMT
RUN Apply image 10.0.20348.1366
# Tue, 13 Dec 2022 23:42:18 GMT
SHELL [cmd /s /c]
# Tue, 13 Dec 2022 23:42:19 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 13 Dec 2022 23:42:20 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 13 Dec 2022 23:42:21 GMT
USER ContainerAdministrator
# Tue, 13 Dec 2022 23:42:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Dec 2022 23:42:41 GMT
USER ContainerUser
# Tue, 13 Dec 2022 23:42:52 GMT
COPY dir:3f9950b949d84f617218d6370bf5d9344385a96fee23c5d0245f1523c4ce092b in C:\openjdk-8 
# Tue, 13 Dec 2022 23:43:16 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:70d3e1cc3b0ea172dcc93064fe6fb9f1f2c8fec6962c90e39991fe89a3c1ca03`  
		Last Modified: Wed, 14 Dec 2022 00:08:13 GMT  
		Size: 122.1 MB (122108200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8147315b2e02d672b57634f58ed466ba0f8747ed03b8d3d40b71ddb17275cf`  
		Last Modified: Wed, 14 Dec 2022 00:07:43 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128acacdc09387e6d962a866eb39cba9f370a7b78476f914473b61887b1d89f4`  
		Last Modified: Wed, 14 Dec 2022 00:07:43 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb439320ce632121ee0f7a844774516fd648bdd0b2fd836a1cfdfc6005e25ab`  
		Last Modified: Wed, 14 Dec 2022 00:07:43 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3e95b11be8e1fe21a48fa16364d0ea798e51169c057d8e09dce1165481076f`  
		Last Modified: Wed, 14 Dec 2022 00:07:41 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787cb91bbed124848cabbf7aff1ceffd2f589690983d067f1b58e55704f45630`  
		Last Modified: Wed, 14 Dec 2022 00:07:41 GMT  
		Size: 85.7 KB (85685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd340f989f9d3800358445c493549519ae3fb410ab35b92c93fe00d61c66e06e`  
		Last Modified: Wed, 14 Dec 2022 00:07:41 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacb218e1083e22321dca7849db530e0f7bfec45e9e88cd4844d75314cbad7a5`  
		Last Modified: Wed, 14 Dec 2022 00:07:57 GMT  
		Size: 100.5 MB (100488564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492159d1634bbf902701fbff35611f7cb80653ce7ad9e4c196c8feda2b5a586d`  
		Last Modified: Wed, 14 Dec 2022 00:07:41 GMT  
		Size: 55.7 KB (55714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
