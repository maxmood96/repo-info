## `openjdk:23-nanoserver-1809`

```console
$ docker pull openjdk@sha256:9193aa927c3e435385def62d52190ab59f4a0e08af8b8efd7de536c8811b8b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:23-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:f3a312fc22d7d9e16ce94d39a67c9b43de584c7a827f8521715ba95e0e05cefc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.4 MB (366393931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a1ead1f42b278f17fa3d2876a84147e67a31a7f6c7dcbc0d8c19b94690097c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Wed, 21 Aug 2024 21:50:54 GMT
SHELL [cmd /s /c]
# Wed, 21 Aug 2024 21:50:55 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 21 Aug 2024 21:50:56 GMT
USER ContainerAdministrator
# Wed, 21 Aug 2024 21:51:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 21 Aug 2024 21:51:04 GMT
USER ContainerUser
# Wed, 21 Aug 2024 21:51:05 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 21:51:13 GMT
COPY dir:7241c997b61b8182ab926524436a25e2a4c14ad587c6199f728ad06ec7b46fd4 in C:\openjdk-23 
# Wed, 21 Aug 2024 21:51:21 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 21 Aug 2024 21:51:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f83c01986bbd54daa4ffb65994ab8c717048d98d6bfa0dfaae0af1f560538`  
		Last Modified: Wed, 21 Aug 2024 21:51:28 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd98b2f9f8289fd43a88eaa21bf6ff449e2d22c5ecb69a2eec49014dfa4b2c0`  
		Last Modified: Wed, 21 Aug 2024 21:51:27 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b80fb7f7eaa5491c330620630df20b08d62aa967868605a78413b495cc15071`  
		Last Modified: Wed, 21 Aug 2024 21:51:27 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d598d9b85dd1f58faf3c38c10e6cbd659a9d3d7f7244e9e095138c976fef437`  
		Last Modified: Wed, 21 Aug 2024 21:51:27 GMT  
		Size: 69.4 KB (69409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4cfa8f06d95723d1df98b8bd001d8d8b3f28744df81026e4cdb2f036043088`  
		Last Modified: Wed, 21 Aug 2024 21:51:25 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3959924613fd66e4cde9435f7cd337a80a5a9cf4efece255587f7bf6c8735794`  
		Last Modified: Wed, 21 Aug 2024 21:51:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d092914a011bbb440f1909101aeb17bed88b199bc7419c971631d8a6c7eb49e`  
		Last Modified: Wed, 21 Aug 2024 21:51:36 GMT  
		Size: 206.0 MB (206041319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357e388e79283ffe6fc72f18ba27b7abbda5aeae85a348124a4defcaaca90909`  
		Last Modified: Wed, 21 Aug 2024 21:51:26 GMT  
		Size: 5.2 MB (5193830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38103b2752684ce18217243367f012ea675e7ebae5b4f87032db188d275d02a7`  
		Last Modified: Wed, 21 Aug 2024 21:51:25 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
