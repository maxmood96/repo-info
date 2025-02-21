## `eclipse-temurin:23-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:dbb115ee8cfefc7f248de9353979b93db1db3bd0ac861298c30611f0db45eea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:23-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:8f04df5e9812916948b179d307bfbac36eb0bf222be5246060cd455e61fdaa5f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 MB (320167648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb440f9f3f6f04ce901322844879517e782afe9e1e3bb658a7bc1b49c6fc7414`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:16:45 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:16:47 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 13 Feb 2025 01:16:48 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 13 Feb 2025 01:16:48 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:16:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:16:52 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:16:58 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Thu, 13 Feb 2025 01:17:05 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Feb 2025 01:17:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af165d2201f27c3c8ecd13eb740ce23daf2453f85f11afd3cd2b21d35718ffd`  
		Last Modified: Thu, 13 Feb 2025 01:17:10 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f0d11e89d655d0ba9d17eb00dc3bcc98840b9588ab2c448224d69153604ccd`  
		Last Modified: Thu, 13 Feb 2025 01:17:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72e7d4e50899022aa8e3f9d04ec97d824b637643b439d9adcc06eeda1d1b24a`  
		Last Modified: Thu, 13 Feb 2025 01:17:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080bf397bd8dfa8b1b6f320bff1642300aeac098cac839f395bb54cf26c64516`  
		Last Modified: Thu, 13 Feb 2025 01:17:09 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570db502148469282b33667cdddb0b156449523abe14dc3924216d6fe1367804`  
		Last Modified: Thu, 13 Feb 2025 01:17:08 GMT  
		Size: 82.9 KB (82899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e02d23a2590ec484479fbdd6162f8792390868e97cdd1920d7b14701c5be2`  
		Last Modified: Thu, 13 Feb 2025 01:17:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ec605d14a9e573b337d368554c4c27dca084bfc9dbacc1ffeca4c4986bfd8e`  
		Last Modified: Thu, 13 Feb 2025 01:17:19 GMT  
		Size: 209.0 MB (209027463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3627b76c6ce75bd294568c8a3e7a3c6e534109219e88a3b8c7962fbcc4c3c6`  
		Last Modified: Thu, 13 Feb 2025 01:17:08 GMT  
		Size: 4.1 MB (4135511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06867a1c9b4769674d25add14ec06fc8e4233b615fd9a220c647178eb4df11aa`  
		Last Modified: Thu, 13 Feb 2025 01:17:08 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
