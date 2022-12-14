## `eclipse-temurin:19-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8d094168633df4d2f7434996a4f25fc57f7a1776d0be4514612c6021bf0b331a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1366; amd64

### `eclipse-temurin:19-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1366; amd64

```console
$ docker pull eclipse-temurin@sha256:10436b6333879a7841908ce0e431129ca8469c639f9281dd4f79b69363b7c1dc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315721567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3babb65f339ca3867e1235602fe924e3560b3263f8b90535e77dcc09bb585fac`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Dec 2022 09:19:21 GMT
RUN Apply image 10.0.20348.1366
# Tue, 13 Dec 2022 23:42:18 GMT
SHELL [cmd /s /c]
# Tue, 13 Dec 2022 23:47:19 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 13 Dec 2022 23:47:19 GMT
ENV JAVA_HOME=C:\openjdk-19
# Tue, 13 Dec 2022 23:47:20 GMT
USER ContainerAdministrator
# Tue, 13 Dec 2022 23:47:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Dec 2022 23:47:34 GMT
USER ContainerUser
# Tue, 13 Dec 2022 23:47:50 GMT
COPY dir:2282de048661e89f3c315adc23c8954e0ca245f9a969462117712d8342758a69 in C:\openjdk-19 
# Tue, 13 Dec 2022 23:48:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Dec 2022 23:48:17 GMT
CMD ["jshell"]
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
	-	`sha256:d1e59eb7a5b4fe8ae96312960a40af592123207c6b91bc9725a5d56edc9dc528`  
		Last Modified: Wed, 14 Dec 2022 00:10:26 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2525b505f9623e25e68733e4851a7234488fd6fbc7d35532e59663d1a22576`  
		Last Modified: Wed, 14 Dec 2022 00:10:26 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197aae1d537644fd1ef15b971e1a44be075a5176964ee577a683f2cc25d32ed7`  
		Last Modified: Wed, 14 Dec 2022 00:10:26 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e0004fe38a6774f98da2c4b08f1e6ddda78814774bc68130a7adf9a3c9cd62`  
		Last Modified: Wed, 14 Dec 2022 00:10:23 GMT  
		Size: 89.5 KB (89453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf8dd32db89784e7ab99fe78051cfb6d3cb5afaf519acc132ef45cb09cd993c`  
		Last Modified: Wed, 14 Dec 2022 00:10:23 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2dd5f6e45477bf84e595637e4efaab1b65cd7644c1e7150af5568e029736eb9`  
		Last Modified: Wed, 14 Dec 2022 00:10:45 GMT  
		Size: 193.4 MB (193446208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac6d79fa8b61b2161b3f01dcfed2f0ca6a432ef1bdf29a9ab45efd9a5eabca4`  
		Last Modified: Wed, 14 Dec 2022 00:10:24 GMT  
		Size: 70.9 KB (70879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a10100fa4c2bee5f1cf131450f350455dde875e2eb0056039cedcc48ce5846`  
		Last Modified: Wed, 14 Dec 2022 00:10:23 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
