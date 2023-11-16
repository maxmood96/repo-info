## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:bb488b100bb7e7d11b1f3ce36a7568a4d4ebf07f18742be5efb5fa9526e7535e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2113; amd64
	-	windows version 10.0.17763.5122; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.2113; amd64

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

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.17763.5122; amd64

```console
$ docker pull eclipse-temurin@sha256:0e6acbb324e80d6e6c4ffb469ff579e0cc0d0d68a4b5d170b45a3432ed96e9ee
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309393720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03be500870dea4c16b6de8b84ad629fe3f655a16fd14a0522e409778386927c4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 01:41:12 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 02:11:58 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Thu, 16 Nov 2023 02:11:59 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Nov 2023 02:12:00 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:12:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 02:12:10 GMT
USER ContainerUser
# Thu, 16 Nov 2023 02:12:25 GMT
COPY dir:fd62014fea6b5cd8b6f3d34ff8f9c5e95aa0ce969b7fd9201e979e77a3abe050 in C:\openjdk-21 
# Thu, 16 Nov 2023 02:12:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Nov 2023 02:12:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5c133738aab79d4c21c47e77cb838e2d00166f5e3e2632177622f67488259`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1f93705bc66be9e7bd16a63fb2083eaa966ce68e0a041581f4f2c060669b56`  
		Last Modified: Thu, 16 Nov 2023 02:36:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19000c594d11a61850151597a4e96bbf27d59ccd9ac158dcbdd52a9a2f7d7507`  
		Last Modified: Thu, 16 Nov 2023 02:36:16 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e3e3a6ccfa0ad291175e9aa8d7b56661c012730cf40821b17a9c24cd81f4ff`  
		Last Modified: Thu, 16 Nov 2023 02:36:17 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea0fa6e5a93366f9ab44f64ea7cb59f6dfba280202e7a1d9d7312959b5be750`  
		Last Modified: Thu, 16 Nov 2023 02:36:15 GMT  
		Size: 71.4 KB (71408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552a786118de89d9b566cf983c928ff2585c7ef7e8a8fa768aae003aa10f563e`  
		Last Modified: Thu, 16 Nov 2023 02:36:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9251d7aadd9f315ef6e9afce35f042dcbdce42465dbb1977c3278e7823153f`  
		Last Modified: Thu, 16 Nov 2023 02:36:35 GMT  
		Size: 201.0 MB (200994805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5023026dfcbabc3ef372028e1206d1ebc3d6dc8a6f024bb71179e771239468b`  
		Last Modified: Thu, 16 Nov 2023 02:36:16 GMT  
		Size: 3.8 MB (3823201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeffc490da1921d44ea5283f9e6610cea97b30ccfb92436da75998a73a9d142`  
		Last Modified: Thu, 16 Nov 2023 02:36:14 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
