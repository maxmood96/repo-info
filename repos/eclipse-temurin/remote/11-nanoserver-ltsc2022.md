## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c7694e996d39662c9550d32edf3a4ba24d759180b489504b9c05a759d27ad59f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull eclipse-temurin@sha256:ae33320e7f9deeea70ef25c7901476a6c574dd0861e4baa5bb22d9267f1efc7f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314689318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c229cd1b6451b6a086f77bf0f742a69dccd69fd0a41405e719827e1fd08c475`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Wed, 15 May 2024 20:32:41 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:34:14 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 15 May 2024 20:34:14 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 May 2024 20:34:15 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:34:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:34:27 GMT
USER ContainerUser
# Wed, 15 May 2024 20:34:40 GMT
COPY dir:8aa740e08efd9dadfa2fb1fd54d653720c8e2097106a2d2f0f8f1f0b127bcc3e in C:\openjdk-11 
# Wed, 15 May 2024 20:34:56 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 May 2024 20:34:57 GMT
CMD ["jshell"]
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
	-	`sha256:44b7ab9e2014bf028d69005e73e9c890b1ced39953355171448e7c3faa8ed787`  
		Last Modified: Wed, 15 May 2024 20:58:53 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d293a70301850fd834eca3494af06656eb7078ab02582b9757ab3a4708ad11`  
		Last Modified: Wed, 15 May 2024 20:58:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e158a6bc02aea2a75b327aa22d4e68dd37603b54860ac95deb7fc75ec67d1ac7`  
		Last Modified: Wed, 15 May 2024 20:58:53 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318982babf657d594a6f92c90d863cbec9ca8b10b1f7961faa76abff80024f93`  
		Last Modified: Wed, 15 May 2024 20:58:51 GMT  
		Size: 98.2 KB (98188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a071dd46f608d64d56b63b93696e4b8bf295ef2fa35dfcb56cb209f96b823f`  
		Last Modified: Wed, 15 May 2024 20:58:51 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc306fb0df9fba9c4078612d0c85cafc95d844cecfbb44e7afd27b933d535f0a`  
		Last Modified: Wed, 15 May 2024 20:59:08 GMT  
		Size: 194.1 MB (194084384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4fdc7bab53e376960b90c691686c357282a8228e932fdd7fe552e666c783065`  
		Last Modified: Wed, 15 May 2024 20:58:51 GMT  
		Size: 74.5 KB (74497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675eba8dc31735c399db93f8ff7020231b0ce9e538ec57298c2525b11584b897`  
		Last Modified: Wed, 15 May 2024 20:58:51 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
