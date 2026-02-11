## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:2f72f78a0f8f5eb8fbb3f6f4efc6998c44676934164e5377e987ebc0758d7cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.32370; amd64

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

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:806e867eb498599efa28d1b6cdbc46cff6bcd151c3c0c656ef16712b806aa493
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166798529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d878b40baf5b67f0f9d0fde7b5cee9b8a3f7171c2c331e75b6682f611fdb79`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 10 Feb 2026 23:30:19 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:30:19 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Feb 2026 23:30:20 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Feb 2026 23:30:20 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:30:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:30:23 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:30:28 GMT
COPY dir:e192ec1627bb02acae941746a6647cea6857b84f7daa4f746913822a0bac9dcc in C:\openjdk-8 
# Tue, 10 Feb 2026 23:30:31 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197769c1803e408434ab708492fd6b579050a976074dbaed3739b29b6199a8ee`  
		Last Modified: Tue, 10 Feb 2026 23:30:37 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eceed90cbd5d1955c6216568900e73817ded358b9473f633f236a4991022da8`  
		Last Modified: Tue, 10 Feb 2026 23:30:37 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d08ae2ad7dbac17533b53ba8d5686a869850f2ea8498812a58c0c61c9120653`  
		Last Modified: Tue, 10 Feb 2026 23:30:37 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cab8b71b0d65da3ea85d644c9aacac85b339e0941a783b90f4089a5827b623`  
		Last Modified: Tue, 10 Feb 2026 23:30:35 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cac05d1dc1e36ef467ba07401c9f2701e89513ed43a7c5e665f6a41de49b009`  
		Last Modified: Tue, 10 Feb 2026 23:30:35 GMT  
		Size: 77.5 KB (77492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354c3e453f871246c520377b6991faa27aab5e03280fddcbda1f2e688b747b47`  
		Last Modified: Tue, 10 Feb 2026 23:30:35 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45e4d96db8cdfdb73d5cf2f22ecfa10528578e502414978388153e6cb4601d6`  
		Last Modified: Tue, 10 Feb 2026 23:30:40 GMT  
		Size: 40.0 MB (39969826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f0f9328d6792737799507cfe090170893f1b227342f311db22333f538a9888`  
		Last Modified: Tue, 10 Feb 2026 23:30:35 GMT  
		Size: 100.0 KB (100022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
