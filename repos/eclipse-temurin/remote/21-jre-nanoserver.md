## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c83ef5aad345dccb1e5eedd676020495b12f4373ebca4b708034794ec6645364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:04b35499968145d5ef58140b415d8963b32042c0aa3458dd8bb1ddaa755e0ac9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245942931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d537e6c4120735d440856378c8d9cba27f36d3d6ce66efe9f6ab7a29cecf024e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:18:08 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:18:09 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 09 Jun 2026 23:18:09 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 09 Jun 2026 23:18:10 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:18:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:18:12 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:18:26 GMT
COPY dir:4940aac187beb0c950977243d0b1d703fc0231f7cabe77dd307cf1e9c831ffc7 in C:\openjdk-21 
# Tue, 09 Jun 2026 23:18:30 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee5a15e6c0ae33d8458f16b5e982a3e6eb3be95d54d8918eb8862671f3dd652`  
		Last Modified: Tue, 09 Jun 2026 23:18:35 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb22b40ceed07a656d6909841ba5c76339ce307eec296fa43701d88806d07aa3`  
		Last Modified: Tue, 09 Jun 2026 23:18:35 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09945c36987cb0d86f3de1bd5694cfaf169665eb3699bd3bd7c95e3dcefe4479`  
		Last Modified: Tue, 09 Jun 2026 23:18:35 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea1ac0b3c8207acb6bbb4a92cc44621895d2cec125486c0d6f4972bfc7368db`  
		Last Modified: Tue, 09 Jun 2026 23:18:33 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0977cf5f56a0dd837a79918db0080c5e0e33fcc42753a1421d14abdba8a591d`  
		Last Modified: Tue, 09 Jun 2026 23:18:34 GMT  
		Size: 73.2 KB (73177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad062f42492fe3da2d38051d6ea21022b83752ef1bb950a7c3e34bf8f27283ea`  
		Last Modified: Tue, 09 Jun 2026 23:18:34 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2250f889d79e8f71552c89da532b2177b4787a6ae7f8a650241a038d98096b45`  
		Last Modified: Tue, 09 Jun 2026 23:18:40 GMT  
		Size: 49.1 MB (49082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4ea58134ffffeeda403f0d8db01380870d52b6e3cab9f44a1a34a9f7fe64e0`  
		Last Modified: Tue, 09 Jun 2026 23:18:33 GMT  
		Size: 113.7 KB (113650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:145bf7cfd345108f6bb296ee097facf05683bf00f79f175034dae90800d540d7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173276889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39407b6f58dd087427f6ee2786d59bc6ad352e05c9c6deac3235c8b0d8d76e57`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:22:14 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:22:14 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 09 Jun 2026 23:22:15 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 09 Jun 2026 23:22:15 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:22:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:22:19 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:22:32 GMT
COPY dir:4940aac187beb0c950977243d0b1d703fc0231f7cabe77dd307cf1e9c831ffc7 in C:\openjdk-21 
# Tue, 09 Jun 2026 23:22:36 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0076bad2aa70237883bc58b47b5081301cd7022a5dccb63bc51e13f0c9dab02`  
		Last Modified: Tue, 09 Jun 2026 23:22:42 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4cb9233359f18638196ba60de66ca8af8cffd49687247da997146cd3dfc340`  
		Last Modified: Tue, 09 Jun 2026 23:22:42 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5c0cd8b3384a3421dd87e70d1d7a5aee9e10abc971f813a8546d8199e41409`  
		Last Modified: Tue, 09 Jun 2026 23:22:42 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504946aaec9eb9d3378e8027b50caebf3c02a28f389a5ad0e0b196e74f656c74`  
		Last Modified: Tue, 09 Jun 2026 23:22:40 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50f84811fead37b440f044fcc0f57518204f04f015dcb79e58fdce4780dede4`  
		Last Modified: Tue, 09 Jun 2026 23:22:40 GMT  
		Size: 87.9 KB (87941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563f04b09bc13e6e847b46d8d37968d9545f72b4c6edea9e7e341c89e0ec1672`  
		Last Modified: Tue, 09 Jun 2026 23:22:40 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480fc4f37dac47b3ee256a42d83a1b310afab4f031fc747652975a17ad281fcf`  
		Last Modified: Tue, 09 Jun 2026 23:22:47 GMT  
		Size: 49.1 MB (49082946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856ff5301bacba6d30f2f1eb61ff518f25b425a8b2c731b73421e6d1dab5160a`  
		Last Modified: Tue, 09 Jun 2026 23:22:40 GMT  
		Size: 103.2 KB (103223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
