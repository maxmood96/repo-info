## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:bb3c76e1a20c5901080851b9e059e7fe213e26bbd6a02ac0a3c0112a7ed15c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull eclipse-temurin@sha256:93032394ed9e0991adce85f1ddc3d682edf559754c20a07b44c92365913b8c39
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147711427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4b035ec34f8d80f94b9ddf504b67fdaf6c3f16836207622968cb1cef8367c4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 00:40:01 GMT
SHELL [cmd /s /c]
# Wed, 10 May 2023 00:49:34 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Wed, 10 May 2023 00:49:35 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 May 2023 00:49:35 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 00:49:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 May 2023 00:49:47 GMT
USER ContainerUser
# Wed, 10 May 2023 00:54:28 GMT
COPY dir:b6e5aca1f3f361bc79d6ed078f0846fae24cf0b7748963379a92b2a6511b98d8 in C:\openjdk-11 
# Wed, 10 May 2023 00:54:40 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b79dd15c5dd82bc10521b9a4e49241f70088bc6edbb286f90be198abea55e23`  
		Last Modified: Wed, 10 May 2023 03:01:27 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55743eb2ae5cd042a272d7ca09db1dc320b97fffa4ff7a6f1f54dafa7878cf5b`  
		Last Modified: Wed, 10 May 2023 06:57:35 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be1c1d26b6510cb6c21b9f715964b78399dc78f00da502aac8e47eac3409d8b`  
		Last Modified: Wed, 10 May 2023 06:57:35 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8319d0c3865d1d122169d35a992638c1cdc3d03bd6576cfeda1ea349058398`  
		Last Modified: Wed, 10 May 2023 06:57:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5313d0be67fb1f48560d21400fa1b69a28bc27ebce45869109c6c43957cea9`  
		Last Modified: Wed, 10 May 2023 06:57:33 GMT  
		Size: 69.2 KB (69204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0189caad3d791abf9f86943871c0eab7b33b58471fd9931654ddffc928f8fbf`  
		Last Modified: Wed, 10 May 2023 06:57:33 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66aa9cd97d9dba033fd98de6cc99448944c0766812f91d9924f2b54525a6129d`  
		Last Modified: Wed, 10 May 2023 06:58:45 GMT  
		Size: 43.2 MB (43172510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7787389bec64869e003aae1025c1df06da9a8b76c0b93cb84f8135d26c5e4aa`  
		Last Modified: Wed, 10 May 2023 06:58:38 GMT  
		Size: 80.0 KB (80017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
