## `eclipse-temurin:8-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:5a25fd43b8cc6f980a6cdafba034022775af1cf4f9146b8ced1e75ee68ceee0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:8-nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:1ab953c3121d3a9dee896a4af6889116f69e4197aff52840122d83049b6a36e0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208273415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da2ec2e49eda4362dff56b5c5b7fa08ee8efb3b7028623ad4379ce56eb93e82`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 00:45:50 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 16 Mar 2023 00:45:51 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 16 Mar 2023 00:45:52 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 00:46:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 00:46:12 GMT
USER ContainerUser
# Thu, 16 Mar 2023 00:46:24 GMT
COPY dir:8214f6b15a617bff549fa1e8e973ad9cf58dcd41804c9c4d00b4aebf5303ecc4 in C:\openjdk-8 
# Thu, 16 Mar 2023 00:46:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5837fe68a36caddf38b0aaa99f4ef20ca36d8dfe2825fa6ffbcf0d38b9d59a`  
		Last Modified: Thu, 16 Mar 2023 01:42:43 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea37c9502d3bcdbbc2eda316dd7dde5525b3c4523d8b934f5fdd7351c4340d6`  
		Last Modified: Thu, 16 Mar 2023 01:42:42 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c839e1c668b550af962755db6bc5dbda77773ff7bf2f0b6e3551aa4e9d034d7b`  
		Last Modified: Thu, 16 Mar 2023 01:42:42 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620cb44234b657aaa3604f3eed13984d197384638b5ac9b4471e430e2549e54d`  
		Last Modified: Thu, 16 Mar 2023 01:42:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bc9547dce91ba94db8caaeaf10a53946ea8a975bbb9ad529fab8913958f34d`  
		Last Modified: Thu, 16 Mar 2023 01:42:41 GMT  
		Size: 69.1 KB (69121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf8194336aa0d18a09a6ca2d7fadacb0b7661b11f336c510037feec43be8c8a`  
		Last Modified: Thu, 16 Mar 2023 01:42:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05432f4af6acb1b34933401f525f3ec2d67176b6a8f9d4331f1f8284b49010b5`  
		Last Modified: Thu, 16 Mar 2023 01:42:59 GMT  
		Size: 101.4 MB (101415502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e58b8307d9bd25fa39ab98d24f5427515947946624aeab5baa350d22543ce24`  
		Last Modified: Thu, 16 Mar 2023 01:42:41 GMT  
		Size: 98.8 KB (98776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
