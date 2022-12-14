## `eclipse-temurin:19-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d920ebd16d47bfca7ef4273361a0b7d7f6558f55c19f8fbc836c93b5ebd4db99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1366; amd64

### `eclipse-temurin:19-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1366; amd64

```console
$ docker pull eclipse-temurin@sha256:a2eb5003c2c014866af75576457e21c4d3dec3a59f29c78a6679da7df2e4e01e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167494027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3853a65d98bb4d45813b0850f1f3a76867d66788f88063641502e62b1b8bbd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Tue, 13 Dec 2022 23:48:41 GMT
COPY dir:f8bde2ca36462d5d41624c06c50c3ec39051aaa6a88f0dabf8bb55af828f5608 in C:\openjdk-19 
# Tue, 13 Dec 2022 23:48:58 GMT
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
	-	`sha256:05a7671d0cb1afa9922c32d918978c19351f53847b95e1d73b38583eeaf79d62`  
		Last Modified: Wed, 14 Dec 2022 00:11:06 GMT  
		Size: 45.2 MB (45221618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35785b90572de1aa70b2f7196ef07376c1c78a5dd3f4758481af38d4033338e0`  
		Last Modified: Wed, 14 Dec 2022 00:10:56 GMT  
		Size: 69.1 KB (69066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
