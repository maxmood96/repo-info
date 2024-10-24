## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0456d3469d26aa9709f4dccfde832c26058557e43069b0bbbfef500bac14f45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:2b2ff6e73fa1940f7f9f15a8a1a23db89c9511001a99b0d60265a1700dc156b5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (165035911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235d8b308f7423c59148bd1c92ff22a5add10bcbf0fdd4c39204f4fde84d9017`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 24 Oct 2024 01:52:32 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:33 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 24 Oct 2024 01:52:33 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 24 Oct 2024 01:52:34 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:52:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:52:47 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:52:51 GMT
COPY dir:4c6d77ca6f58a330005c5f34389fe1882335ea3db28c021259e868cb18ddb756 in C:\openjdk-17 
# Thu, 24 Oct 2024 01:52:55 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23402c945805daea80708909a46c7bdfc65dc575d9523a3058a22edb7fba68c7`  
		Last Modified: Thu, 24 Oct 2024 01:53:01 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198916dcc8a6348d3bd6f39214b473877f234ef373e2af58507de36657c472e3`  
		Last Modified: Thu, 24 Oct 2024 01:53:01 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4fc89158183d39d4707c0dc26231373d51ddcc98d313c54a9e8c1845aa0039`  
		Last Modified: Thu, 24 Oct 2024 01:53:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c986d1a8418bb84b6d4e747a8ca2e6416c8266b902f2da10b342b104bf4a60b8`  
		Last Modified: Thu, 24 Oct 2024 01:52:59 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c8d67465a2357c6c5e43e32572b580388d5146f16483385c194941aa0b374d`  
		Last Modified: Thu, 24 Oct 2024 01:52:59 GMT  
		Size: 72.9 KB (72918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4550f6d76999fa8f876cc09b303df1dd5866caab5ff9b6f75c1914d20a6d058e`  
		Last Modified: Thu, 24 Oct 2024 01:52:59 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9eb7a16fe27386a49e3fcee069a50af1604d4400d53ea7e56c0021231dd121`  
		Last Modified: Thu, 24 Oct 2024 01:53:04 GMT  
		Size: 44.4 MB (44358290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f208df2622fab682e97b71e07036fb0a7cdc83448aa74d62e2d44a7eee5408`  
		Last Modified: Thu, 24 Oct 2024 01:52:59 GMT  
		Size: 88.5 KB (88546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:d9865270ac13a60f34a3ff39f1beef978db9fca155a460d89a9c883d714cc904
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202495054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1b6a4e60d70c851b902e155b72dd720c9a53946948f0dad0745fc45284bbb0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 24 Oct 2024 01:53:10 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:53:12 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 24 Oct 2024 01:53:13 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 24 Oct 2024 01:53:14 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:30 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:35 GMT
COPY dir:4c6d77ca6f58a330005c5f34389fe1882335ea3db28c021259e868cb18ddb756 in C:\openjdk-17 
# Thu, 24 Oct 2024 01:53:40 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514585b6eeb53fb96e1e6a5d559f0eef2c59b5e47c8352440f585f93cff17c7f`  
		Last Modified: Thu, 24 Oct 2024 01:53:43 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36572ae012f0357e8a09d38e1e3251f3e098c61a3424cbf37ac3e549372749af`  
		Last Modified: Thu, 24 Oct 2024 01:53:43 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7d886e6a483b32f43fce3298e5c8152894c7a624322e0c9a5b7aab8fadf443`  
		Last Modified: Thu, 24 Oct 2024 01:53:43 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbbf04d19aed0b80f25eceaf3fa5271a31835dd5dbf82fd4e2739dcf0637f0f`  
		Last Modified: Thu, 24 Oct 2024 01:53:42 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb274ff678953cf0dffbf4744cc2e2ec91aff8748f50715cb11f04a900a339e3`  
		Last Modified: Thu, 24 Oct 2024 01:53:43 GMT  
		Size: 66.4 KB (66393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333ca45e1c1c07b092767497df511eda93d63a7ae4ccfad0e3e1e2c4b7c4e75d`  
		Last Modified: Thu, 24 Oct 2024 01:53:43 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd401f0acd0069bcc02c07e88760fcdc8e7c613e62c9253e536b39b13a8a0ea`  
		Last Modified: Thu, 24 Oct 2024 01:53:47 GMT  
		Size: 44.4 MB (44357851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c6ae4c09c5d5ad02c2705b701a28be616170a1cc32acb8759ae1cf87999f68`  
		Last Modified: Thu, 24 Oct 2024 01:53:43 GMT  
		Size: 3.0 MB (2972076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
