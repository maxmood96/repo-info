## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e1e8b7d93bdaef8439f9c3105d4e39b112d3dcc75e2bb03cd89d0555f14182b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:f08c45b9467990a8e2c92acfef378c3be8c6cad24d55da6702fee5fc2a8cd7b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321649719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd32d84843e940e69f4533a030fa3ace377747ff4e7b0f62ff9d561f2f79ffab`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Thu, 05 Feb 2026 22:39:32 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:33 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:39:33 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 05 Feb 2026 22:39:33 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:39:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:39:40 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:40:02 GMT
COPY dir:7dbbb550790b7446baaa5767cc14c2e1895a96b2462584273935c311b414f284 in C:\openjdk-11 
# Thu, 05 Feb 2026 22:40:10 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 05 Feb 2026 22:40:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c7039741d89d842613be48c41b10cbc4947353296e42bf0bf9cbd59096fdfc`  
		Last Modified: Thu, 05 Feb 2026 22:40:17 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ba19e467519ef2d288cc482542a4f83a83033addb26e62f6c5d1f119b92ac2`  
		Last Modified: Thu, 05 Feb 2026 22:40:17 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b1d626810a07918098194226fc97fbf96fd867b8ab2c61d535a9284975db75`  
		Last Modified: Thu, 05 Feb 2026 22:40:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62102eb44a81390a9dbaabe8b3f5a19139661a4c69751a0717fa1e1efec96ffb`  
		Last Modified: Thu, 05 Feb 2026 22:40:17 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1049dff3686ef276d13b14b2f8cc1d177bd6c755391b73eed55c1b78db64fe3b`  
		Last Modified: Thu, 05 Feb 2026 22:40:15 GMT  
		Size: 71.0 KB (70972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8590faaf4022424fa3cc4c293d953e01ab0a9db522d6f59cd5bd69a04400d5f1`  
		Last Modified: Thu, 05 Feb 2026 22:40:15 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259152ef145b7fc27ac7242c8e53f4dbf2483819511e877efa199bd5e14a3066`  
		Last Modified: Thu, 05 Feb 2026 22:40:28 GMT  
		Size: 194.7 MB (194723103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfdb89e1225ff128515d32a52721b4b9171aaea1cc4d6d5de13ae264160a704`  
		Last Modified: Thu, 05 Feb 2026 22:40:15 GMT  
		Size: 152.4 KB (152434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7b30106387da3c12403e253481c971c0bbbe7480725d1ba0f203cb11a90ff3`  
		Last Modified: Thu, 05 Feb 2026 22:40:15 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
