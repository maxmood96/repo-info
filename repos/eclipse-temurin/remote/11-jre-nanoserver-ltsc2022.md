## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b6f9c3e76221106cc79c2d1b3b428f98b554779aa40e7aeec16784b342f7fb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:65b7cea1f9ccc77dd080b6e2e90687f815ca49587227a16ee4e045bb52a52bcc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164270994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c439a5413f0749a341e8cd358a4076341ec2e17059cb0945057cbaabb5fee82f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 23:18:24 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Wed, 10 Jan 2024 23:18:25 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Jan 2024 23:18:26 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:18:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 23:18:36 GMT
USER ContainerUser
# Wed, 10 Jan 2024 23:19:24 GMT
COPY dir:32725fa0f7edeee10e8937816f70b588636369ca6a0eb68560cc5c3b2b3f76d9 in C:\openjdk-11 
# Wed, 10 Jan 2024 23:19:35 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:c6e143c42b4550c9dd98d53d07a6e7e468b8a75e216cd70375bc0f0cf9ea84b6`  
		Last Modified: Thu, 11 Jan 2024 04:19:37 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0985559ff18ff3ddad4ed8a1f472ab78b2b8f94bbf3874daeac5450ac6cfd0e0`  
		Last Modified: Thu, 11 Jan 2024 04:19:37 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc87f76aed872301743ef2895913a2b02712aa574317489dd3ce20faabc32091`  
		Last Modified: Thu, 11 Jan 2024 04:19:37 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea63e927d75425d29af4e73d85860f4f653b270427acc2f9600f627e0724c4d`  
		Last Modified: Thu, 11 Jan 2024 04:19:35 GMT  
		Size: 89.2 KB (89178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b900601d476437863c71ce34b26134091419d354da04b4ac0b38f895d0aa4e9`  
		Last Modified: Thu, 11 Jan 2024 04:19:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890579dd958d34ee8217e8905004c311f9ba416803bde4f8bf6da86193b80519`  
		Last Modified: Thu, 11 Jan 2024 04:20:15 GMT  
		Size: 43.3 MB (43337080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40d998bbbee8be8d6726536322b2e649795d1eb48664dca933d36d025e29a7f`  
		Last Modified: Thu, 11 Jan 2024 04:20:07 GMT  
		Size: 69.7 KB (69655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
