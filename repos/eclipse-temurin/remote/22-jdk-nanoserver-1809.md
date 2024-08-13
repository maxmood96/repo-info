## `eclipse-temurin:22-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ec563d449f4d240018128d5899b67745b916a2181a9046858de5cf362e2a4601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:22-jdk-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull eclipse-temurin@sha256:89c3212c1c596281a97c3b0755f68c324e0201f4ac10c3c43c1dc10293207fc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358617138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19417d476cb04f9c76ba55d0603a5737a2185b67660d680645f3fe96a6fc2f89`
-	Default Command: `["jshell"]`
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
# Tue, 13 Aug 2024 20:15:48 GMT
COPY dir:bb8037d92e17293fdab4a72c09c9eb83e6a7b620b5e832c71d656bbaf7bd694c in C:\openjdk-22 
# Tue, 13 Aug 2024 20:15:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Aug 2024 20:16:00 GMT
CMD ["jshell"]
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
	-	`sha256:c16c9c22de80131f72a5f04ede717e92be7f5b671b9e129c442e0730c36bbdbc`  
		Last Modified: Tue, 13 Aug 2024 20:39:03 GMT  
		Size: 199.6 MB (199622747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff24670c633e1f41961141b744b054729ff21664a0a8257fad4ef83bb961ed8`  
		Last Modified: Tue, 13 Aug 2024 20:38:50 GMT  
		Size: 3.8 MB (3836038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59011ac4dcf7531eb50e4b63043bc895ff35954b81b1205ee028d040599dd46`  
		Last Modified: Tue, 13 Aug 2024 20:38:49 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
