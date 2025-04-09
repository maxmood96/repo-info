## `eclipse-temurin:24-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1932c1826015b32b32ff3940d45c2a86f5ba34ae48dadae80738dee33c322e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:24-nanoserver-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:3bbc3e3bd864ec3b776ce4faf3227c79fe3a1fb715fc447a0c6902d0e89ec7a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327646860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98392ed01f6fc59d57444de32550c17b7caac53d7d73e68044e9517010f720df`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:18:16 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:18:17 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 01:18:18 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Apr 2025 01:18:19 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:18:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:18:23 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:18:31 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Wed, 09 Apr 2025 01:18:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 01:18:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49afa67ee8fbfc00c93f889d47ed7a472fdc767a94d580f3f169dafe6c3cfa2`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d3e42f13e523cf73059c3b59e2adeea54050c54049bb5f18bc97df5b12c1f0`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493a3871065d26b8e44f6008e4bc5a76006909cb8192cf15a980b14d2e13aa6d`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe276d3de633e8ca8be2e6abb8d9897fb753c6989cb4d967eb66da1708cc17e3`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7be48ba4e61770f2a54495e23132a0eca0273c3be120057996889650469a4dc`  
		Last Modified: Wed, 09 Apr 2025 01:18:41 GMT  
		Size: 77.6 KB (77571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f728c86efa53c02cf32345e2429b5358af46348efe09fefab946872cafcfce9`  
		Last Modified: Wed, 09 Apr 2025 01:18:41 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a773a527c3f916b3ffaaece8264c65345dee34f322a15d5bc83616f12df909`  
		Last Modified: Wed, 09 Apr 2025 01:18:52 GMT  
		Size: 137.4 MB (137355571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba764c8af9f3a294ae2dd71e7137bbb2a7cf69009a58114f4a5f77a58bd8ed77`  
		Last Modified: Wed, 09 Apr 2025 01:18:41 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7ae72265d75f6229747ed6be8eb9035f5b4433b80de20ac34583d1d5359c10`  
		Last Modified: Wed, 09 Apr 2025 01:18:41 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
