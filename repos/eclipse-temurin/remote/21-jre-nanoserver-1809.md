## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:4e284c51081dcf1acb8930d0f6f0bc017602f4ab587a8214c12db334e2170c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull eclipse-temurin@sha256:2f91a90b9c552826ffe81da9847a024bda70a854fe52dc6fc973a2c84b67b604
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156810477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223b634e3f271762a5453dd2870f956d6c1087b5d6e734016cd2f7e84903da5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 19:41:52 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 20:14:57 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 14 Feb 2024 20:14:58 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 Feb 2024 20:14:58 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:15:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 20:15:08 GMT
USER ContainerUser
# Wed, 14 Feb 2024 20:20:45 GMT
COPY dir:a5c64f66204a1ce40e58093b44657f9abbd9eecac263988d919d778d3cf84131 in C:\openjdk-21 
# Wed, 14 Feb 2024 20:20:56 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddfc54d18bb5861232283d3ff2ca5e214ade28a46dfcf6c1e7c7243809e5e85`  
		Last Modified: Thu, 15 Feb 2024 00:06:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5ac0c0039279c81ef8a0b73777c70eb0f4154275b16090c8d8dec0b0b5f7d`  
		Last Modified: Thu, 15 Feb 2024 00:15:02 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36850236406ffaebeaf74d5c2af7a8bb2637218fb04780435d349be93ed40816`  
		Last Modified: Thu, 15 Feb 2024 00:15:01 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417a71895a6404699264769031380768677b589482a450b1e835203f3ab11b4d`  
		Last Modified: Thu, 15 Feb 2024 00:15:01 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6471b0637a32e9a57c629c854d2e57b0626e0f458f9b191e94eb4bff975d5551`  
		Last Modified: Thu, 15 Feb 2024 00:14:59 GMT  
		Size: 67.6 KB (67568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797ef2bc893d6f044556f13a437c95f1432144cc0f7b015cbb179b2344846182`  
		Last Modified: Thu, 15 Feb 2024 00:14:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258724218769b8ff8d03536b39b587b234af5b22241c1acea7cf90702fe2c447`  
		Last Modified: Thu, 15 Feb 2024 00:16:19 GMT  
		Size: 48.7 MB (48749978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab38c2f0f1b086bb975cfb22029824fc5834b07bdd899167c79e5cf07b60d011`  
		Last Modified: Thu, 15 Feb 2024 00:16:11 GMT  
		Size: 3.4 MB (3365545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
