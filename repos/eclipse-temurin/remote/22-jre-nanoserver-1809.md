## `eclipse-temurin:22-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:88209f3fe990ac1f886fa8a4892d222aa0f63ae94f76e4f75b9c8fae7f46bd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:22-jre-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull eclipse-temurin@sha256:3d3bb05a81e5471dfd404100b8d2b613e8df9018ad5a9cbec505a94ff27dead1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206906530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57267d5b401cd36073882811bc44dbf5b25b644c57bfee905f56f3b1f946851`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 19:40:26 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 20:15:26 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Tue, 13 Aug 2024 20:15:27 GMT
ENV JAVA_HOME=C:\openjdk-22
# Tue, 13 Aug 2024 20:15:27 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 20:15:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Aug 2024 20:15:35 GMT
USER ContainerUser
# Tue, 13 Aug 2024 20:19:32 GMT
COPY dir:65be971618b84fe71c044bdca6efe8a2b46f4ab6c5b677a6f304a9c5505af541 in C:\openjdk-22 
# Tue, 13 Aug 2024 20:19:40 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee91db53edb9eaa638d7d926c33dc3d39a0bedf5ace2c9ff25f8c413bc3ea2c6`  
		Last Modified: Tue, 13 Aug 2024 20:30:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4139004ccb09c46c0a78f1acfad59c42dc6830f7837b9fae693e70486cec9b4a`  
		Last Modified: Tue, 13 Aug 2024 20:38:51 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74cd9dd405ac44c2c74cac05662d15aabd047bb05dfcd079eddd0fdf9397462f`  
		Last Modified: Tue, 13 Aug 2024 20:38:51 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952e36034cf2f21f0ebc0a19f516c2ea2399b27cd5eb659ab2734bf0442784df`  
		Last Modified: Tue, 13 Aug 2024 20:38:51 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fee17c4fa73cda0dc174692fa5773f30ed1d9548ef419f907609d58bb956dc`  
		Last Modified: Tue, 13 Aug 2024 20:38:49 GMT  
		Size: 68.9 KB (68883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881865bcc6b5a452bfcb67069a79ea06aff73bb2d05bc9ebf531f469aae147c0`  
		Last Modified: Tue, 13 Aug 2024 20:38:49 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059f2c773f780ec0e62c8333a639999093d5720a36d4f47988a17b118ad82e16`  
		Last Modified: Tue, 13 Aug 2024 20:39:53 GMT  
		Size: 48.4 MB (48367755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ddcc6ff3e1978d5b92cfb7826953f12d5b5a1a2ad2c464fe738d3b895bcbe8`  
		Last Modified: Tue, 13 Aug 2024 20:39:47 GMT  
		Size: 3.4 MB (3381503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
