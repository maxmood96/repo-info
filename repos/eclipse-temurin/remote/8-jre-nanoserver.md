## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:bbdebd3ba21d0a10b138bb65c8e3d0a690c67d8e251568aeaba45871e43c7a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:60aa2df0b2f06c77d09684f3a16596ac7904f8c92962bcd72b8f6b8a78ba3767
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160683465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03180636df28b0aad9a827368e79ebd60d70297d3f6d6ca9d6e256487fc8a732`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:11:44 GMT
SHELL [cmd /s /c]
# Thu, 10 Oct 2024 00:11:45 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 10 Oct 2024 00:11:46 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 10 Oct 2024 00:11:47 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:12:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Oct 2024 00:12:01 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:12:43 GMT
COPY dir:9cd76711a1e21cd053ac2280c0520b18fc7c9ba73d3efc8192b2b62cbbddbbff in C:\openjdk-8 
# Thu, 10 Oct 2024 00:12:56 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96818114ce85fcf68e8af61951767bf11ed374ffe6a9023b6150122fbad46d51`  
		Last Modified: Thu, 10 Oct 2024 00:32:47 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702dd5af34f5a288dc9f423ce99dc45f825e5908a5abd9751b25875f6d11356c`  
		Last Modified: Thu, 10 Oct 2024 00:32:47 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e73b3fbec6ab963baeaf37902cf7c4cded0dd4140d7cd8304507e705b4885cc`  
		Last Modified: Thu, 10 Oct 2024 00:32:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e01992d787cd675fe8027e387b62953278cc86f9ff2848c3f5caf257ef8247`  
		Last Modified: Thu, 10 Oct 2024 00:32:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b3a5e8c630fbee27654249fdc4ab04572b3db9697412f448e3318b2a6f4b0a`  
		Last Modified: Thu, 10 Oct 2024 00:32:45 GMT  
		Size: 83.7 KB (83726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f39cd6234ef7bb6fab55d144f75a01753b9f32029fb9de2ef237ff22cbcd4b`  
		Last Modified: Thu, 10 Oct 2024 00:32:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab871486cfae70796216f5d97fa665ad8e6ce93eae17915e07468fedd0b707f`  
		Last Modified: Thu, 10 Oct 2024 00:33:23 GMT  
		Size: 40.0 MB (40012126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8eb86582fb65b4d107f441e307fbdc58f6bf669597aab8388a19e04f7507e55`  
		Last Modified: Thu, 10 Oct 2024 00:33:18 GMT  
		Size: 70.8 KB (70843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.6414; amd64

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
