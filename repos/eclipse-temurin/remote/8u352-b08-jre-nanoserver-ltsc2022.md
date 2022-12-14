## `eclipse-temurin:8u352-b08-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7a5d4d8ecf580576f558f2f1dbc807bbc9d7fa741379ec9dec93aa7ab443bc97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1366; amd64

### `eclipse-temurin:8u352-b08-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1366; amd64

```console
$ docker pull eclipse-temurin@sha256:b2b6097a4b75b4ed307a5a5dbe2073ff09d73a66f4d485180d5c0512d6f226c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161578743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17d5c4928947d4dfe369ba789a242c2a1232372ce1b4638eb4fa5c8183f5223`
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
# Tue, 13 Dec 2022 23:43:28 GMT
COPY dir:4e862dd3e9e3173048336ba652726d009cc7bbbadd67bc711cdb421cf611c5ab in C:\openjdk-8 
# Tue, 13 Dec 2022 23:43:46 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:500e62c8245ed650a1c47d2e0777ef48d33088130bde5f6548c17f1ce0ed6c59`  
		Last Modified: Wed, 14 Dec 2022 00:08:31 GMT  
		Size: 39.3 MB (39322588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782a2a0f6ca9c97f90de8946b9c9a074592e491de8fd2a9c27595c9e331c0842`  
		Last Modified: Wed, 14 Dec 2022 00:08:24 GMT  
		Size: 57.0 KB (56996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
