## `eclipse-temurin:8u482-b08-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:8191ae36e25bb322352ff8efc89ce0810c5dca463b06e710346ce353f05ffa7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `eclipse-temurin:8u482-b08-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:2844ce98673660cf544d4ba4081293da7dcb2c03bc24c7fab51975056c3ab582
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239420794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62999a38d19a458742eecc9ee9b802ebe8f314a54ddfd0b5ff902956ff8da61`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 10 Feb 2026 23:36:00 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:36:01 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Feb 2026 23:36:01 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Feb 2026 23:36:02 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:36:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:36:06 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:36:11 GMT
COPY dir:e192ec1627bb02acae941746a6647cea6857b84f7daa4f746913822a0bac9dcc in C:\openjdk-8 
# Tue, 10 Feb 2026 23:36:15 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3dce7d04b54012ad336c4257e236aae7eacd37339fbd951a05adc4cef9ef819`  
		Last Modified: Tue, 10 Feb 2026 23:36:21 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6509e7172117a8021fdfff53a624c6f61d53295a007033dba2ad2e8e466669a9`  
		Last Modified: Tue, 10 Feb 2026 23:36:21 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc183a8bd8a968a642e8bae47757d4e80d331d9f848ca7121c921f6bac819b59`  
		Last Modified: Tue, 10 Feb 2026 23:36:21 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587fcf41204766e221f286f7557fba2c4f34a1c88c7e5f6f63261da408c1cb04`  
		Last Modified: Tue, 10 Feb 2026 23:36:19 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59390fe4925dcd65a77d90a7491e6a32772a40a70751e14143ef1876e436c9d`  
		Last Modified: Tue, 10 Feb 2026 23:36:19 GMT  
		Size: 72.2 KB (72195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83618e39c4b0a1558e8148bb9f62de82c0b6c7e280ae6292b054ed37571c6c5c`  
		Last Modified: Tue, 10 Feb 2026 23:36:19 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8243dbd9e1d18ea5669cd90ab9e4ef026de17e49db76bf5d1fe02afec50d243`  
		Last Modified: Tue, 10 Feb 2026 23:36:23 GMT  
		Size: 40.0 MB (39969651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b10a5c1743fd7b18f034064aac4b947050db5866b68da56b8b17445a82c159f`  
		Last Modified: Tue, 10 Feb 2026 23:36:19 GMT  
		Size: 122.0 KB (121951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
