## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:a062fbc8962e1f4de8adbbcd5aefc1e4cd3576fd6d7b9de20be32496165cf2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull eclipse-temurin@sha256:f72c3b6c59563cbbb7009ee27185b69b1852e870ec42c9cdea70e237c5982e5d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297736380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77efe92f2ef760a2a72176585efc61d16c89e2e0d0f6655ac8c15f504d2d6bed`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 02:29:44 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 02:43:30 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Wed, 13 Sep 2023 02:43:31 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Sep 2023 02:43:32 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 02:44:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 02:44:01 GMT
USER ContainerUser
# Wed, 13 Sep 2023 02:44:17 GMT
COPY dir:bc17122f89ccac6825b72157f71faf8ee914101def60109a37803e17ec7fe7f6 in C:\openjdk-11 
# Wed, 13 Sep 2023 02:44:55 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 02:44:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5bcbc9b0f0398bf8f14c235b24ba85d9acacf855518119cd1ce338a235a15`  
		Last Modified: Wed, 13 Sep 2023 03:36:33 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d7b7d75fbd464f57c815eba5759b84eba992e1181ac8610a11600a5786dc6e`  
		Last Modified: Wed, 13 Sep 2023 03:39:19 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d61eab367cb741e60d2d29fba6fb78fb995e331fa95085d4d3f07bbb952132`  
		Last Modified: Wed, 13 Sep 2023 03:39:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13aeec5d9d499bda0b5c4d038cfa0327de9f4b4cc27b15dd7691916c4072f2ef`  
		Last Modified: Wed, 13 Sep 2023 03:39:19 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85639b62914801d5dd7c6087de9c28dc7441ae3a4e051e63cce0dd799db485cd`  
		Last Modified: Wed, 13 Sep 2023 03:39:17 GMT  
		Size: 79.2 KB (79167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a9e31c407277bbc8724eef8acfd862576506b0a203e2f190c99bfbe6c88a96`  
		Last Modified: Wed, 13 Sep 2023 03:39:17 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e60e56fa7bc066434c4384874c4139aa89ad18ab27fa14cdbb3aa360f0cf7a`  
		Last Modified: Wed, 13 Sep 2023 03:39:38 GMT  
		Size: 193.1 MB (193092024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce04b207b42ce90300fda5572bf56ddfc82870a3ef927365a9c5ce68df2738b9`  
		Last Modified: Wed, 13 Sep 2023 03:39:17 GMT  
		Size: 65.7 KB (65722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46b3dc1ed1e74a0cb7ca98d48ab4d19438341d7c3e8e570fa4418d9b6a63be0`  
		Last Modified: Wed, 13 Sep 2023 03:39:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
