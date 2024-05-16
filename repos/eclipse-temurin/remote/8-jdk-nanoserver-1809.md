## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ad8b080c409a33ebdc983d1f042766436726beb6e5c56161219c72be7a516d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:aa28fc6b6f0a51876a8272d572d8022d3b6363fe35d176ae9abe0b392a195d9c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256782829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0881b15951c2e605a34e1ad94c3f7c7cfeb4e2fbe7f1bf21573efa4bfc704ed5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 19:42:01 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 19:42:02 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 15 May 2024 19:42:02 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 May 2024 19:42:03 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 19:42:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 19:42:16 GMT
USER ContainerUser
# Wed, 15 May 2024 19:42:26 GMT
COPY dir:5498972beafb1de3e4749bc87b064f8ce9cec472aae9e7d0f4643a99f48638da in C:\openjdk-8 
# Wed, 15 May 2024 19:42:40 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6a511fea8e874efc08e5058ac5b12b6433c36ba6570862a619dd80cfb0e190`  
		Last Modified: Wed, 15 May 2024 20:45:52 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74976804c8dbcdaab371bfee5867397bcc1534f2e5075f4f2177e57220af6a32`  
		Last Modified: Wed, 15 May 2024 20:45:51 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcaee39153f7d403b580a55761fdae993ede00f35ce692d4812487921b966b0`  
		Last Modified: Wed, 15 May 2024 20:45:51 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823d1a2911a4cbbc904707b3cc18799385d37229fa7f8b553a434df806541903`  
		Last Modified: Wed, 15 May 2024 20:45:49 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d9613d36d5bfb005a981e899b80f521af784fa912479aecb529f26bddee63f`  
		Last Modified: Wed, 15 May 2024 20:45:50 GMT  
		Size: 68.5 KB (68502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9dd4a26438bc32bc60490598537fa55bbee9900825ab2aa551e84da2ddf8f4`  
		Last Modified: Wed, 15 May 2024 20:45:49 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a781a4cc7a2b41891ec7fc7fe008ef3bc09fe9ac1870b8360efbabffee6b46f2`  
		Last Modified: Wed, 15 May 2024 20:46:03 GMT  
		Size: 101.7 MB (101686327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b306afaa4fcb2cf300f9919994e61c21b80dd08283ce2e41b8aea2433a357318`  
		Last Modified: Wed, 15 May 2024 20:45:49 GMT  
		Size: 80.8 KB (80833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
