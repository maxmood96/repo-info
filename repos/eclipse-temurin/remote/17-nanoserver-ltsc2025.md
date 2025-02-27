## `eclipse-temurin:17-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:ec86c2d8dcb72dc52f5c30764cf069b852107aee05d5d0b3c5b6c2eefa6b2465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `eclipse-temurin:17-nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:e74bece81c9b83e6c7befd3b63d101a64bc8c319ce208165dec9c93e62444542
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.3 MB (393301829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6925b5d50ffe8b9db335c6fafc08e337a71e66374a52a647aff67940b580df3f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:13:25 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:13:26 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 27 Feb 2025 19:13:26 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 27 Feb 2025 19:13:27 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:13:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 27 Feb 2025 19:13:30 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:13:36 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Thu, 27 Feb 2025 19:13:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 27 Feb 2025 19:13:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b79ed0e3582afc14457b50f854db26ed7756424f145898eef1b1b8f0ad3eb88`  
		Last Modified: Thu, 27 Feb 2025 19:13:50 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a2017eef3ce0ce78e38fdc1bc97086abeb89080316df3a1194db7717b3ada4`  
		Last Modified: Thu, 27 Feb 2025 19:13:50 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaae2e70ae4c0d6b25e943c7cda1871afec6e2db232b3e1168465c1b2290bc8`  
		Last Modified: Thu, 27 Feb 2025 19:13:50 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1579eeb73ecf7ef8043bb961cff408233ca2e20832d0bf7938e1d705abfc7e82`  
		Last Modified: Thu, 27 Feb 2025 19:13:50 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6924521e40be21be3e436e145d1cd6b50b7712f05f797944aa40943b07859f9b`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 75.9 KB (75852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbe07143b0e5fc0dbf11be60a5ade673a0e8f4ac1c6abe295d49679d0f26bb9`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3abe1901b34db8011c5790f95a1330a2162ddb4e07d5efebd78ba467c103b6`  
		Last Modified: Thu, 27 Feb 2025 19:13:58 GMT  
		Size: 187.2 MB (187235035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d50c828a6895ed5bd9a42339111cb6c2bbedfc52f9a0e945804091de5c7001`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 94.3 KB (94341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f31e55e4ea92b9a52c2453ae3312db7d5a41c32ebff427c7c6315259d57e85d`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
