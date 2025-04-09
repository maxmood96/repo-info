## `eclipse-temurin:24-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8e18118e9e6b4045370f1c020dc3c0aa4c923a7f3878ab6e37114cb4c68e7988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:24-nanoserver` - windows version 10.0.26100.3775; amd64

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

### `eclipse-temurin:24-nanoserver` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:d340a1e7bedd694c710d2893e2801d51955514936dd996e708761f942117300f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248773980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc7f1893867049f3bf9d72c70d6f3ba95a711db6b276eb32e857556bdb459fe`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:50:05 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:50:06 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 01:50:07 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Apr 2025 01:50:07 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:50:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:50:10 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:50:17 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Wed, 09 Apr 2025 01:50:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 01:50:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70586b86c0ac1b1d73d626bc586c4857b2f083b38eff7cc2d41ca91a9eaa418`  
		Last Modified: Wed, 09 Apr 2025 01:50:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7050f5a661edda42cd766ce92d5f8f1473c4cc4c8547ebbff8a4df276d087216`  
		Last Modified: Wed, 09 Apr 2025 01:50:30 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589cf869f284c6e4ba012867eff822a5887d46b2a9c8895a9f39606a62ee2a28`  
		Last Modified: Wed, 09 Apr 2025 01:50:30 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d45a6b5a0adb575292668d32689538205665cbfa55632ec1dee0999c7d9c1b`  
		Last Modified: Wed, 09 Apr 2025 01:50:30 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7293695835d3070bf66e066c722138780a18b8734c51d575ff9790313ab3a4f6`  
		Last Modified: Wed, 09 Apr 2025 01:50:28 GMT  
		Size: 71.9 KB (71864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f33f604b936b2c11355a6eceb14b8675155a94a0db085f7d99daaa696cc5ac6`  
		Last Modified: Wed, 09 Apr 2025 01:50:28 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d06ed132b8eb0cff2c74b80df97f44d762a0428017aa22c37495300a876b62`  
		Last Modified: Wed, 09 Apr 2025 01:50:39 GMT  
		Size: 137.4 MB (137355657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f339d9945f24dd9927c0674c75d6fa9b9e2d9740b78f45cf9e52bf61314ebab0`  
		Last Modified: Wed, 09 Apr 2025 01:50:29 GMT  
		Size: 4.4 MB (4417674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2465182f3139b66e15f619b7038187a055d12ba1346e9d632548fbaa5786c3c2`  
		Last Modified: Wed, 09 Apr 2025 01:50:28 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
