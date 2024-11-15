## `eclipse-temurin:23-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a229373cbbacde3841545a41fbdf2b64a29d3cf97ee6726e521cdfb6ee426e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:23-jdk-nanoserver` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:05cd95e4141e7a036ff02324a408326d3bba0efdfcd6fc4e5ee24716b9542af0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330902226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62263d0488607465c07c0322b3320f068790cc94f9a9249ad7eba09f24f9b0b5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 21:20:56 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:20:57 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Thu, 14 Nov 2024 21:20:58 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 14 Nov 2024 21:20:58 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:21:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:21:01 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:21:09 GMT
COPY dir:997f391ddfc9feaa4d1b725e1babc077a76dd78201dd489cc8f03fe767c19cd0 in C:\openjdk-23 
# Thu, 14 Nov 2024 21:21:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 14 Nov 2024 21:21:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8780a220b5740acb077252cbc052b6a36bbc2f15b2d21dc7fc3bc917a18c4f58`  
		Last Modified: Thu, 14 Nov 2024 21:21:22 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd9880e952238f9623c8054fa0ed57c165404de0fc7883f56f752bd5f46fa69`  
		Last Modified: Thu, 14 Nov 2024 21:21:21 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f622da3d2acca3acd676a37e332203670f47ba05cff2ce523d5fca2ddecb5f`  
		Last Modified: Thu, 14 Nov 2024 21:21:21 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3a02038ce03fcb1d009deb9461729775a2394f2584f49767f4ad1da9aac42`  
		Last Modified: Thu, 14 Nov 2024 21:21:21 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc6fea2c041a53953ad5e8d7d1d32609f67a525dda2b2db49da32237d6216fb`  
		Last Modified: Thu, 14 Nov 2024 21:21:19 GMT  
		Size: 78.4 KB (78432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49b52efa0108464bf10942acb73bebd5ef3835c71e42a3a05a2c023ed6d0129`  
		Last Modified: Thu, 14 Nov 2024 21:21:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2044c66480ac2a6013c44d146e102b8de79c4a0bc47723bd2fc1a51897f50e40`  
		Last Modified: Thu, 14 Nov 2024 21:21:30 GMT  
		Size: 210.1 MB (210105801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac200a01383ee49f2d9ef70f9599cc2dbba4f2b397cfcd2cd9563d0779aec72a`  
		Last Modified: Thu, 14 Nov 2024 21:21:19 GMT  
		Size: 106.9 KB (106855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb93b5dcb2392d6874ddf5bd1178ba6513aa06d92ad0c944e67cd701b5300ac3`  
		Last Modified: Thu, 14 Nov 2024 21:21:19 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jdk-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:e87bcab93efb5c52d3e14a3b2d6572346962351a1f53961f260992a50888c791
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.5 MB (369527049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5fac6b633c45f5ef4050d75f26fdb3fd31dcdf87a9dd9d868be11c8093e9ed`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:15:55 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:15:56 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Thu, 14 Nov 2024 21:15:57 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 14 Nov 2024 21:15:57 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:16:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:16:00 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:16:08 GMT
COPY dir:997f391ddfc9feaa4d1b725e1babc077a76dd78201dd489cc8f03fe767c19cd0 in C:\openjdk-23 
# Thu, 14 Nov 2024 21:16:13 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 14 Nov 2024 21:16:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47e0137a90f51f01e521ab2e7b5c0ef11eaeb87c265b1530c2c023514a9d906`  
		Last Modified: Thu, 14 Nov 2024 21:16:21 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfcf0c31be4d8ea80d9bc4c30fa39364932654eaabda35225e97c97228f0cef`  
		Last Modified: Thu, 14 Nov 2024 21:16:20 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81573ccad998da9f5bda85bad0d765e461b14bd6371952c3516ad91778886319`  
		Last Modified: Thu, 14 Nov 2024 21:16:20 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efacb73e8f0a0d07810cb0a1b9d3d2f4c29ac55094ebc82f8a6165dd43a1194c`  
		Last Modified: Thu, 14 Nov 2024 21:16:20 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df47957ddd18aaf26bbcad3992b35c1e568a903c22a9529353af6c1dce48ae7`  
		Last Modified: Thu, 14 Nov 2024 21:16:18 GMT  
		Size: 73.1 KB (73139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8d212ae29ef0ef93eb67b632fc96db7451e4b95b93159d5e20061a673115c5`  
		Last Modified: Thu, 14 Nov 2024 21:16:18 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9e76a175bfd89673146bcece0f043137861ec9f26a0ef708669d75d9eb8e47`  
		Last Modified: Thu, 14 Nov 2024 21:16:29 GMT  
		Size: 210.1 MB (210105917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6eeb6c5cdb962581b152d9b15453e91eada6d40a0bc3ce7850e61fe6571cb4`  
		Last Modified: Thu, 14 Nov 2024 21:16:19 GMT  
		Size: 4.1 MB (4127278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f608006a33f45a6f83744173a73f33408346bf9d28e5ab143696925daebf5bed`  
		Last Modified: Thu, 14 Nov 2024 21:16:18 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
