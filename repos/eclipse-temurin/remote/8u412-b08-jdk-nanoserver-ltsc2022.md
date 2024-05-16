## `eclipse-temurin:8u412-b08-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:fff8bf580b5bacfce585df4c15d5f8199dd043f8de1cddd61ddb0c4e4e26373e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `eclipse-temurin:8u412-b08-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull eclipse-temurin@sha256:4848e85487e9486a7b0cfeadf0c73fdb95722a402cc11daa583a8db71102db23
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222275622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243f51acb355e5fe3261800b33361ad6563ef9a2bae0787c91110d350ba062a5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Wed, 15 May 2024 20:32:41 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:32:41 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 15 May 2024 20:32:42 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 May 2024 20:32:42 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:32:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:32:57 GMT
USER ContainerUser
# Wed, 15 May 2024 20:33:07 GMT
COPY dir:5498972beafb1de3e4749bc87b064f8ce9cec472aae9e7d0f4643a99f48638da in C:\openjdk-8 
# Wed, 15 May 2024 20:33:21 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5560c76ac3d9aa2d8a6dbf79d443a7e1d170aae31c940cf791c9b532d5756a1`  
		Last Modified: Wed, 15 May 2024 20:58:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dbb40521687111c936a988f66d47ab3fd30a19ebbd9370a6f3df121a767de3`  
		Last Modified: Wed, 15 May 2024 20:58:04 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4b147667e0c3a3f801d405e1be4947c2e08ddde3a3f99a29d7263588f2e54b`  
		Last Modified: Wed, 15 May 2024 20:58:04 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befc41f88d0673d002077cd4d08dcaba7064f5be6a8f1f5b5f16cfabf9d6a8f8`  
		Last Modified: Wed, 15 May 2024 20:58:02 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d8653e3a805a6d89f416bc4d1ec1a06d03b1e0fd77135400831a968f9a00eb`  
		Last Modified: Wed, 15 May 2024 20:58:02 GMT  
		Size: 75.0 KB (74953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28741ab0414b29a8d8737bf2082c9d696e2857a855d2d6e8ab156be0eea11ea6`  
		Last Modified: Wed, 15 May 2024 20:58:02 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f519b69021a8659277d10faf08f175e0d4ed0db26c546ab3251963c74b5f9d5`  
		Last Modified: Wed, 15 May 2024 20:58:14 GMT  
		Size: 101.7 MB (101708278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cde9c4b5a7e531225c0281c68753de28fb7ea9111d03e2649efaa2e33a9adb6`  
		Last Modified: Wed, 15 May 2024 20:58:02 GMT  
		Size: 61.4 KB (61368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
