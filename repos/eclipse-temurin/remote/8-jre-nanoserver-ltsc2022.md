## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1e350fb16ddc4364ce2feeed1b7601410c115873d9692f517c1b03b8ace8726c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:b691040e5b394507f8a4b004ef9073363b49fa9654e48be841313caa6607f22c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161032870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdd542a5ab9ae7b555587c489aae1853f451d5554eb90e4bfa76842fb9d50f8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:53:23 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 21:53:24 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 24 Jan 2024 21:53:24 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:53:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jan 2024 21:53:47 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:54:30 GMT
COPY dir:db8ed4bc6cf3fc1a9a530d737bd8bcda792821f4f1e3e610cedaee77629ebb36 in C:\openjdk-8 
# Wed, 24 Jan 2024 21:54:43 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5f2601f3a3b05b34c1f8683e3c9ea81ea63dbe1b04c37b85d09170f020fc0`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bc6f55d94ad6babb64b648ddd4e3d6d8072a6266be4c48a8381f0c374a7724`  
		Last Modified: Wed, 24 Jan 2024 22:11:23 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8550800dcda4ebc8d1cc88204963b26f3442312b25f671aac3d9560aa39b4df2`  
		Last Modified: Wed, 24 Jan 2024 22:11:23 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520937eeb616efcc621cdf2db195eef5183f5b7517ef9ccf1a110e4eb1c01c39`  
		Last Modified: Wed, 24 Jan 2024 22:11:21 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c41f39f8cd5ecc958ed1cad2cb8d774b184e8e399d3ad9b793e5a98904d4a6`  
		Last Modified: Wed, 24 Jan 2024 22:11:22 GMT  
		Size: 85.9 KB (85881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605c359866d83e1868c6b725a8294b3ff8f2e73ae0272190ab7c80a25ceb1d9b`  
		Last Modified: Wed, 24 Jan 2024 22:11:21 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc21c241b24e3b3202722169a41841937db29fc3d82928c48ddccc9abcfd5bbb`  
		Last Modified: Wed, 24 Jan 2024 22:11:51 GMT  
		Size: 40.1 MB (40113273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89c515faf860c6be9701258b9d061a98a38c8bb26ae7f6be84d4ab7fe96f761`  
		Last Modified: Wed, 24 Jan 2024 22:11:46 GMT  
		Size: 58.7 KB (58704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
