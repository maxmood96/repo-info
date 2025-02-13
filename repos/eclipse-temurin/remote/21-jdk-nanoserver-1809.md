## `eclipse-temurin:21-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b4e0783e88373fb93d5abdf961faa93d731115ff03431dadd88f5e2cb28af32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:21-jdk-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:100420620581a722ebb05d1f8d6c27cab5b7d8129a1640aea06b4d204e88752e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312346774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15144b86aa90121a84861f1c1c214ae9b64e325095faa1d3e8c2cc121b9b8ff6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:18:14 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:18:16 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 13 Feb 2025 01:18:17 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 13 Feb 2025 01:18:17 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:18:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:18:21 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:29 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Thu, 13 Feb 2025 01:18:35 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Feb 2025 01:18:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef990e33f6502a31a71735eb7c1b6f27432384e26c796fb8a14d8c303d39044d`  
		Last Modified: Thu, 13 Feb 2025 04:15:07 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac6461a0ac59119e9f3255b5e56e3a4c8361825a474b97c6be42b8e5473fe9c`  
		Last Modified: Thu, 13 Feb 2025 04:15:07 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7178e770251e023d63c23eff825b653cb41fb3118542eaf96fdd0b05e26dc0b3`  
		Last Modified: Thu, 13 Feb 2025 04:15:07 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f9723ebebb0f813627b781f38a377542b0c6a57b5d12cf5ba44835840d13f7`  
		Last Modified: Thu, 13 Feb 2025 04:15:07 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf493e4c6ac40985dfb863190240a87c70d9ae99abb09d93c04cd8e13522cd8a`  
		Last Modified: Thu, 13 Feb 2025 04:15:07 GMT  
		Size: 86.4 KB (86389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bc7c45e5d9cd9279d4dbc14f207a84eb89518a5193849db7c9499c76807be4`  
		Last Modified: Thu, 13 Feb 2025 04:15:07 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d1885082e8fc26a462866c8ffd1ecd075041aaa6790d0b5ac510f325119d02`  
		Last Modified: Thu, 13 Feb 2025 04:15:23 GMT  
		Size: 201.5 MB (201475573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8976399611c589069cd401d7ed02b7eded6bf7aaebb5ebb7df217a296b42751e`  
		Last Modified: Thu, 13 Feb 2025 04:15:08 GMT  
		Size: 3.9 MB (3863088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf73e4daf5d238c890d9ab23d5ad66c8e6a999d32668cee1195c0e217b5b6db`  
		Last Modified: Thu, 13 Feb 2025 04:15:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
