## `openjdk:16-ea-28-nanoserver-1809`

```console
$ docker pull openjdk@sha256:8e79a1fb3b1ad690a2e72c0991041ae94f13286849c3d51a780bc9092ed3c669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `openjdk:16-ea-28-nanoserver-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull openjdk@sha256:0e8a3b984fb4f2bd4bf64a4e0b6cffa39a654ae33c6ffa6028bba9a9c4574abf
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285110412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725026e14e52963c796e99ff5cb5bb893290f009dca14f25d0e5cbc0d2e66f18`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Dec 2020 08:05:47 GMT
RUN Apply image 1809-amd64
# Wed, 09 Dec 2020 18:58:23 GMT
SHELL [cmd /s /c]
# Wed, 09 Dec 2020 18:58:23 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 09 Dec 2020 18:58:24 GMT
USER ContainerAdministrator
# Wed, 09 Dec 2020 18:58:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 09 Dec 2020 18:58:40 GMT
USER ContainerUser
# Mon, 14 Dec 2020 21:29:19 GMT
ENV JAVA_VERSION=16-ea+28
# Mon, 14 Dec 2020 21:29:43 GMT
COPY dir:6bb9e6df3e2b447cab9898bacaa092b8570ccaf4974329d19ed787d458818f10 in C:\openjdk-16 
# Mon, 14 Dec 2020 21:30:14 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Mon, 14 Dec 2020 21:30:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:21be49aa856f07be4e0a677b988e43c04bd595a3c858e58b6c364477bbbf7222`  
		Size: 101.3 MB (101264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fe9a51a0164bd1c063cbda08c4e22dc4f5d04a8047a3951d7441f37fb93c57f2`  
		Last Modified: Wed, 09 Dec 2020 19:34:04 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8993beeae33a05d68775319a4b9f9df44ac08ccfc62cb15113a36b06ad62d1f`  
		Last Modified: Wed, 09 Dec 2020 19:34:02 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340da9582f81cba4147b5da6d500dacd9f3ffdd520c3211dfb20153cd4ae71fc`  
		Last Modified: Wed, 09 Dec 2020 19:34:02 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f848f35781549a8c193011c95049cd95311b558af39d0f8057a5b460a459488`  
		Last Modified: Wed, 09 Dec 2020 19:34:02 GMT  
		Size: 64.6 KB (64579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636f94045101715dca150f5013879c45929dec9e849eac5b53631727e42bb8a6`  
		Last Modified: Wed, 09 Dec 2020 19:33:59 GMT  
		Size: 873.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fca08504cb8693a30fbbf40cd2dbaaecf9f367f2ddb386aff25487e79e224fb`  
		Last Modified: Mon, 14 Dec 2020 21:43:00 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56fe7e1b409eec1d35a20ab7aad44eb6cc2fe18131bae74118e5f2d65183737a`  
		Last Modified: Mon, 14 Dec 2020 21:46:18 GMT  
		Size: 180.1 MB (180114967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990cf7985fb94d4a5c74cf80960268bbc6f1f33e6f8835539ec148251c3fcc41`  
		Last Modified: Mon, 14 Dec 2020 21:43:02 GMT  
		Size: 3.7 MB (3660792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d9185eff067c39c17ed340b854ebb74bcdeab6571c8c81d1f34432b8c05aac`  
		Last Modified: Mon, 14 Dec 2020 21:43:01 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
