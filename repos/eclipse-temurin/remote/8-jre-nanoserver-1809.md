## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e790d8c311b185601311cc42fa0b6234fdb5b076170175a0a58a720df1d32795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:f1c6555ba33a9c3712d122b8b4e2ef4981bc1c4f0e5e6d4b89684f21287f825a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195217564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4298c3041f8321b76cebd633ba040df47b3d419444ded3d77dfaaec2e110b486`
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
# Wed, 15 May 2024 19:47:20 GMT
COPY dir:2b748c8b95a49802258ef446e3948354b660cf39e9ffa8b2cf36461ec042c5c0 in C:\openjdk-8 
# Wed, 15 May 2024 19:47:31 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:023884ce9cf8a843681159bf8335237e0f4c011448096654d578758b3d85b79a`  
		Last Modified: Wed, 15 May 2024 20:47:09 GMT  
		Size: 40.1 MB (40113556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94374f60c65b74781ee06d59bf5c33d41cc1734101c144a3b398bac9dfbb385`  
		Last Modified: Wed, 15 May 2024 20:47:03 GMT  
		Size: 88.3 KB (88339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
