## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:44c8b7821f7294650598a3332d3a06d42132fc9f3f4500019b219f51043586c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1366; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1366; amd64

```console
$ docker pull eclipse-temurin@sha256:495e9bbf751c2537168fad2b3b5a94a13e536509faa81d7b43aeb2bc549579a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165209222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ae6e45d18b10f25fd697e1b8c2ab264cc2d281a67f549901f1844b2a2b3b56`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Dec 2022 09:19:21 GMT
RUN Apply image 10.0.20348.1366
# Tue, 13 Dec 2022 23:42:18 GMT
SHELL [cmd /s /c]
# Tue, 13 Dec 2022 23:43:52 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 13 Dec 2022 23:43:53 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 13 Dec 2022 23:43:54 GMT
USER ContainerAdministrator
# Tue, 13 Dec 2022 23:44:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Dec 2022 23:44:07 GMT
USER ContainerUser
# Tue, 13 Dec 2022 23:45:15 GMT
COPY dir:f12bd30467bc1b7f61ca05a6124e6eb838888f3685c56f372d6fed2165b193b1 in C:\openjdk-11 
# Tue, 13 Dec 2022 23:45:34 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:edb94d83b63b52ad108115f9f418e8e892eba45f96177f5fc313292b015bc683`  
		Last Modified: Wed, 14 Dec 2022 00:08:42 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d9005d9a7cd8ec9093aa3eee2fee7817562bfae5e8904ab28c81e3ec335dd0`  
		Last Modified: Wed, 14 Dec 2022 00:08:42 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2165df34ac053d89d45e349d186b50eedd9f3cac512257edc6caab4d25dc4d16`  
		Last Modified: Wed, 14 Dec 2022 00:08:42 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52739d4fc84669becc74b1e504faf4bb34f213b9ce78766adc5ece4154d05c99`  
		Last Modified: Wed, 14 Dec 2022 00:08:40 GMT  
		Size: 75.8 KB (75769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fae8e48107aaf4a924d7597a62d28f75b362ee701e63d11dac65622a2faf012`  
		Last Modified: Wed, 14 Dec 2022 00:08:40 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f2641a973ed114ee0d52389eb9cc8d4a0ebbc1863480504dfc8deceafd7f7e`  
		Last Modified: Wed, 14 Dec 2022 00:09:22 GMT  
		Size: 43.0 MB (42960274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6b025df0bc25de500fb3ab69ae4ffee37895ae7f375ab36b23992cb4274af1`  
		Last Modified: Wed, 14 Dec 2022 00:09:13 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
