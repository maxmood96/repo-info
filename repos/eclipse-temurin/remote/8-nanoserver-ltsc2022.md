## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:5e7f318437a9dea645b12b216713cecac44a9ba6e3ef0c6e549d4767580ff527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:f1edcc58144726cfc1c3628d3d09a38fc1ac67584f69b643b68069a4debebf81
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218725879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9a0bb9d77ecdb7775b31abac38a45d293c373beb141534beb75581f436e740`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 16:28:17 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:28:18 GMT
ENV JAVA_VERSION=jdk8u342-b07.1
# Wed, 10 Aug 2022 16:28:19 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Aug 2022 16:28:20 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:28:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:28:39 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:28:51 GMT
COPY dir:770d4c58725f903fa5cc3374e6a3f654e24baf27258320561cb0479514743464 in C:\openjdk-8 
# Wed, 10 Aug 2022 16:29:10 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f1e06146ab0490d235fe89786637467a4b71853ee428e8740ea6efbc536c47c`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3394ec2ce30ad34ba1f49293a6dae79cb2eed817cbc7b40694ba7f6d0e1d05`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2718daabf741b8f95d00a685a921166dc7f53af3c1d38115bd3405295d4f4531`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55010f95ce79cb5009b93d7e9e5fb07b9e3765f7f8960626a4a7ac5b0ada1b0f`  
		Last Modified: Wed, 10 Aug 2022 16:48:38 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc238e7ac783a8731bbe122740ed009e39631d26b7f40760ee09a1cb8312868`  
		Last Modified: Wed, 10 Aug 2022 16:48:38 GMT  
		Size: 84.9 KB (84914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c5449a8cac2ad9691a9433c12495a32c0c1c72a8f595eb0bf4302559e7bc43`  
		Last Modified: Wed, 10 Aug 2022 16:48:37 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc29225b2bc177de4cd1138448dd9b9614f40bcf78b38352b180381948628493`  
		Last Modified: Wed, 10 Aug 2022 16:48:49 GMT  
		Size: 100.5 MB (100476250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9dbf04179569ff3b9c00d46d15058744d61ea080dcc84c10e96d647bc0abf0e`  
		Last Modified: Wed, 10 Aug 2022 16:48:38 GMT  
		Size: 70.5 KB (70493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
