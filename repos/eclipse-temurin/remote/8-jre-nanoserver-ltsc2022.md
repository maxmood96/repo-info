## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:47aebce84ea800e48162271da49d900a6decb1ec65f773ecee2deb2be6e977bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull eclipse-temurin@sha256:f8461cb7af7e5d43cfee8a1b47d213e313d826eea3342196d78b22765d08adc1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160686724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7843d13d5cdc2b972bc674a7ab10e510a016981f24d53e2be693074a737055d6`
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
# Wed, 15 May 2024 20:33:39 GMT
COPY dir:2b748c8b95a49802258ef446e3948354b660cf39e9ffa8b2cf36461ec042c5c0 in C:\openjdk-8 
# Wed, 15 May 2024 20:34:06 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:b50d267a94e1dc89a6a2343e2b2aee26ea91d9c66515c7d55519c8213461197b`  
		Last Modified: Wed, 15 May 2024 20:58:42 GMT  
		Size: 40.1 MB (40119365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64f7908fe3a0307e798dbb9befc752219f6d84f5a7aa076b8a1e3f06c5e3bd5`  
		Last Modified: Wed, 15 May 2024 20:58:36 GMT  
		Size: 61.4 KB (61383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
