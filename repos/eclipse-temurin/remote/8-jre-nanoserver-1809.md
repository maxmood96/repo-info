## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:7113f698bf5546d619da9ee7f35cf62c2b5e179dab05deec8dbba932c0ab6067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull eclipse-temurin@sha256:32ec9eb080b76b5550eb00df1c443c5dbeccae30aa08cd72d63209231bd5180b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142254850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4e2af8151042bb48ed9ac67c521b9f1f805cf1e2003332a9abe9e1f544c92`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:33:30 GMT
SHELL [cmd /s /c]
# Tue, 11 Jan 2022 21:33:31 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Tue, 11 Jan 2022 21:33:32 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 11 Jan 2022 21:33:32 GMT
USER ContainerAdministrator
# Tue, 11 Jan 2022 21:33:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Jan 2022 21:33:49 GMT
USER ContainerUser
# Tue, 11 Jan 2022 21:41:15 GMT
COPY dir:f43ebde5893522b38a147191e5e447aa435ef67c7d947aeb3e536f25bc61cdb3 in C:\openjdk-8 
# Tue, 11 Jan 2022 21:41:29 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6cc5785ab09c66739c3205c3a26410f1cf4bf85c377fa81b240e754cf0659c58`  
		Last Modified: Tue, 11 Jan 2022 22:44:40 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57dbd86100c2f89c898ccb22fe49143f18ac91d265650aed86bce6ca4c440b2`  
		Last Modified: Tue, 11 Jan 2022 22:44:40 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304fb8a87b93b0c55df8e416ba8eb9e9f7c7d839f8352fba177b78db62d27961`  
		Last Modified: Tue, 11 Jan 2022 22:44:40 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3c4ec70ba8edb5640c63ab1a2a0fcb04216749b103d00170450683853ca825`  
		Last Modified: Tue, 11 Jan 2022 22:44:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af2121f00d2777a3444ebaace92855a88b75bb1709cb45ae9282cf6fbb10246`  
		Last Modified: Tue, 11 Jan 2022 22:44:38 GMT  
		Size: 68.4 KB (68365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f44e345e8a9816ad2c38838029d414a029a1d60c67879ca9a779019dcbafd4`  
		Last Modified: Tue, 11 Jan 2022 22:44:38 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b967e800da53b401a12991eea0af762985a42fd5da21dda3a77d4f8c4069614a`  
		Last Modified: Tue, 11 Jan 2022 22:47:55 GMT  
		Size: 39.1 MB (39086252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db72cb3b0e64065ef593ac5e490ad699c1b8f46979304212871e0b30dfdaa33`  
		Last Modified: Tue, 11 Jan 2022 22:47:48 GMT  
		Size: 80.3 KB (80283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
