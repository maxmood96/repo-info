## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:5070addd0d129888c7dc6a53c5f38f0e6cbb21af66a8e228ef0339544dd8bdf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.6414; amd64

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
