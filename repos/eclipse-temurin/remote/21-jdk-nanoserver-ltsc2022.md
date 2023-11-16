## `eclipse-temurin:21-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:acf58b5e672eb1bd5fc3f0516420ddfd9895f52c1643934abb46cbb3c0e7a9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull eclipse-temurin@sha256:2bc6e3648df59498526dd4ce11c3df66ff4e30bdb165cc82e77f2b7506cb7228
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321891507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec0a258a292111360a300041b864c9f8fe3a9d5f84f165f6b0ced3a45275a37`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 06:09:19 GMT
RUN Apply image 10.0.20348.2113
# Thu, 16 Nov 2023 02:17:18 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 02:21:27 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Thu, 16 Nov 2023 02:21:28 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Nov 2023 02:21:29 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:21:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 02:21:41 GMT
USER ContainerUser
# Thu, 16 Nov 2023 02:21:58 GMT
COPY dir:fd62014fea6b5cd8b6f3d34ff8f9c5e95aa0ce969b7fd9201e979e77a3abe050 in C:\openjdk-21 
# Thu, 16 Nov 2023 02:22:11 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Nov 2023 02:22:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1ca4fbe907f22e883670decfa8d7f4490a79a995bb83a6c286248c21d61a62f5`  
		Last Modified: Tue, 14 Nov 2023 21:13:36 GMT  
		Size: 120.8 MB (120753560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2f0edb58e1876347bbad88c907697db94e172aa6ff4a38560ccfb68d72aa86`  
		Last Modified: Thu, 16 Nov 2023 02:37:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d38c761f22514cb74d62a362aaceaff5643e34635a1a205276b38a73369c4b0`  
		Last Modified: Thu, 16 Nov 2023 02:40:14 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc6362d58554adddf75c17e64c65c7b198ae1bd1c13586007a811be2a76bac9`  
		Last Modified: Thu, 16 Nov 2023 02:40:14 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a189975ca6a65bd0bb69aa62ade1d685a91b9cd3b00370016b814c89109f24b6`  
		Last Modified: Thu, 16 Nov 2023 02:40:14 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a1e989bea1378ebde2905b30edb6311c06cfefa79673c6cbefbe0c1d4e073b`  
		Last Modified: Thu, 16 Nov 2023 02:40:12 GMT  
		Size: 78.9 KB (78886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740931fbe3e3d4b7f0e8347e60522d74ea0b079c2bca51844161f8336c7d8b6`  
		Last Modified: Thu, 16 Nov 2023 02:40:12 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18af18c36b199d231f7a4ed24ba0a96cd9c2b761a31f4fc970cfdadc3da7f7d6`  
		Last Modified: Thu, 16 Nov 2023 02:40:32 GMT  
		Size: 201.0 MB (200991594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136759886f0ae905fb50ce9a8b1e818523311f309e1963974dbabc4144fe058d`  
		Last Modified: Thu, 16 Nov 2023 02:40:12 GMT  
		Size: 61.2 KB (61159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362b642985b33943b400a976d7145078dcf3d88d614c46e6f177a5b582327758`  
		Last Modified: Thu, 16 Nov 2023 02:40:12 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
