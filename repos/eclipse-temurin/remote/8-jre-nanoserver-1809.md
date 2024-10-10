## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:c0ea979dd4f790751d0339b414d156c2221478320a45734147dbc2a68f22c70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:b33fb9bc9ee3455f80e200673b83108de84313be99d4397dd6a65d8ffb0635b9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195280579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918f3f40efdcfc4fc435054a73a4b988494433702ce7f335a97b29c027259bc5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Wed, 09 Oct 2024 23:37:31 GMT
SHELL [cmd /s /c]
# Wed, 09 Oct 2024 23:37:32 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Wed, 09 Oct 2024 23:37:32 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Oct 2024 23:37:33 GMT
USER ContainerAdministrator
# Wed, 09 Oct 2024 23:37:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Oct 2024 23:37:44 GMT
USER ContainerUser
# Wed, 09 Oct 2024 23:41:18 GMT
COPY dir:9cd76711a1e21cd053ac2280c0520b18fc7c9ba73d3efc8192b2b62cbbddbbff in C:\openjdk-8 
# Wed, 09 Oct 2024 23:41:28 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6adfd98d9a05d48859cfa5f6e1dc162be56797c9e86e7647518192a16af3d27`  
		Last Modified: Thu, 10 Oct 2024 00:20:41 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28727a74df40b2463e1a5c1193cfe1cdb7fb960e48c494fa660b684f819aa7cb`  
		Last Modified: Thu, 10 Oct 2024 00:20:41 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27762712ab2901171f32f9f1dff0dda3fab334a6afe54dd0b39410e30b87be64`  
		Last Modified: Thu, 10 Oct 2024 00:20:40 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf55c537b39610846d2772cd1ad8a8a7a7330caaa2f96f10bdf95e4c0d61795`  
		Last Modified: Thu, 10 Oct 2024 00:20:38 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818b97d2f0d5ad2b52d52882f709abfa91d0ee153d932d4c1464df9f5096ad85`  
		Last Modified: Thu, 10 Oct 2024 00:20:39 GMT  
		Size: 74.7 KB (74666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b7c61cfcfe51d03564ff77bddcbd529b38927e2eae0d3b61951e505f209157`  
		Last Modified: Thu, 10 Oct 2024 00:20:38 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d909c87c4c0cb7d3d0099d122957cece2fc59fc8cdf3b1ed431a1a04502e7d5d`  
		Last Modified: Thu, 10 Oct 2024 00:21:52 GMT  
		Size: 40.0 MB (40019128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b8dfef6777d050522d02c828eaa151b33e50aa45db27b9b38831c1df1d62f8`  
		Last Modified: Thu, 10 Oct 2024 00:21:47 GMT  
		Size: 87.4 KB (87376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
