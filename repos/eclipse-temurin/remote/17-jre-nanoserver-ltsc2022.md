## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b19f26c34e6543344acdde5bf70a7ea9a97da0f6665626b6e9577a03c9cc33e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:80c916166ce6bd9fa189a7699dbf292d4abf4f12a50aa3b6d7999306cd2ef61e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166550005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5985797d2f9ef1daf33db408549a4e35f4fd38516e0aaccfebf9603aedc235`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:12:22 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:12:23 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 09 Jul 2025 19:12:24 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Jul 2025 19:12:24 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:12:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:12:28 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:12:32 GMT
COPY dir:6f6fcea1890c098492beafa1d6f550d144651035b2d4a098a7658e545737cf82 in C:\openjdk-17 
# Wed, 09 Jul 2025 19:12:36 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d231ca54f3b932f08267d84575328ebfa44973e62bdc7f60425770703a9539`  
		Last Modified: Wed, 09 Jul 2025 19:12:56 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9fea1ddfe14b526ab94aa959e43bac05904229ea3f11f8e4b6900d0b489626`  
		Last Modified: Wed, 09 Jul 2025 19:12:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bb2be7499d21a2de5c958818c6f6d3b47ee4c587230dbb8f3cbd92b11477b9`  
		Last Modified: Wed, 09 Jul 2025 19:12:56 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fe651bebb821e20a6cdc394fc628f61d8500f2afad2434b5a8efe131a71410`  
		Last Modified: Wed, 09 Jul 2025 19:12:56 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555c183d0ebe12059a3b2a511dedc5eac6a2a4499167234a1dd02505c3404579`  
		Last Modified: Wed, 09 Jul 2025 19:12:56 GMT  
		Size: 76.6 KB (76558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f16e247e7c53a28ea38f72ecc983e3dfa7d58a881aee4b36da47166933532db`  
		Last Modified: Wed, 09 Jul 2025 19:12:56 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacc2a0795d3e7d76a784a88967c3a32217532d9bfc2ae9b2949e9968730f5d7`  
		Last Modified: Wed, 09 Jul 2025 19:12:59 GMT  
		Size: 43.7 MB (43736420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5299b070d4cb4c72fc04f547330c3decc0b422515ca32ebc556b5d61a11084`  
		Last Modified: Wed, 09 Jul 2025 19:12:56 GMT  
		Size: 101.0 KB (100978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
