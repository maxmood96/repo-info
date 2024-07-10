## `eclipse-temurin:22-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:15ad6b67a2955996c4e77ef62645e0f6e163c66d0b16ac9b525a9b57533d5a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:22-jdk-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:02af1034bc661877a313d05773a4c22ad721abe3f4dee5132db588d8a3352e1c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359049544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271d01dd516fa247cf1c40b70eddd115f2b81e10c64b01e7df5c3fda377d6b3a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:12:43 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 10 Jul 2024 17:12:44 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 10 Jul 2024 17:12:45 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:12:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:12:52 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:13:05 GMT
COPY dir:b848142647370c7b57f8798114952350d05bf467cc96eb22cf5219409c8a4580 in C:\openjdk-22 
# Wed, 10 Jul 2024 17:13:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Jul 2024 17:13:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267a93688093f80ca8dad6f6eee6a284f8b5cc9d9513f090ffa870b2e76ee406`  
		Last Modified: Wed, 10 Jul 2024 17:37:34 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8513278cb5f417bcdd9bd49c4201bbe5858b11ff5e9dbc5813ca94e05cd84370`  
		Last Modified: Wed, 10 Jul 2024 17:37:34 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0957646dc3ce5ff5b9bab0b4ee6f9fca3d8e02e59851c100f30dad72ed7dc7`  
		Last Modified: Wed, 10 Jul 2024 17:37:34 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a82a3bfac767fb92f27a365bbdaf517aa0abe5a47399225fbb263332cdca67a`  
		Last Modified: Wed, 10 Jul 2024 17:37:32 GMT  
		Size: 69.5 KB (69480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c5d402c03451a70f00fdd335f9e0fa44e4b669193e85452132172681d8d5fa`  
		Last Modified: Wed, 10 Jul 2024 17:37:32 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1ca3c2b7c8b7b783e0cc75d843668168826cd1420f28c8b052c89d08067756`  
		Last Modified: Wed, 10 Jul 2024 17:37:49 GMT  
		Size: 200.0 MB (200044535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3131968e8d7a1cdb06fa1bd953a283ceb0eee8e38999bcba8569dcbaf4dae42`  
		Last Modified: Wed, 10 Jul 2024 17:37:33 GMT  
		Size: 3.8 MB (3847177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15907e58d89e912569353645a80f01e5113ed23094944920ce7dabc3d2ea7d8`  
		Last Modified: Wed, 10 Jul 2024 17:37:32 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
