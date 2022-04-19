## `openjdk:8u322-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:8948560a393d816b65844c2a19b85d3fc177a00442612af374536b96b69380c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `openjdk:8u322-jdk-nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull openjdk@sha256:44e9ec3a4b13388930aee2bb3e9bb21ef2eda862752d164e7b28b44b864e16ed
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204333533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2d1ca16749f4a9b0011725f060d0f697773734a3a054e7f6f1e5be8e7f55ed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 15:16:11 GMT
SHELL [cmd /s /c]
# Wed, 13 Apr 2022 17:21:37 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Apr 2022 17:21:37 GMT
USER ContainerAdministrator
# Wed, 13 Apr 2022 17:21:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Apr 2022 17:21:44 GMT
USER ContainerUser
# Wed, 13 Apr 2022 17:21:44 GMT
ENV JAVA_VERSION=8u322
# Wed, 13 Apr 2022 17:21:58 GMT
COPY dir:70b73c62c79b1e3a83236c8add186d48955c92966a80012af2e52ff572318d7b in C:\openjdk-8 
# Wed, 13 Apr 2022 17:22:08 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ea4009814dceb50337c66614a6008cfc2fb73ce53e62162bce071ef6ea1adf2d`  
		Last Modified: Wed, 13 Apr 2022 15:58:06 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65fb95ee42514e5278fb1f68d4225d0a5bba71921defb635d841ca30789226f`  
		Last Modified: Tue, 19 Apr 2022 01:19:34 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b00dbd36f2154a4eabea44e9a5d88c98927e03b469bb16de373838d0f29d1e`  
		Last Modified: Tue, 19 Apr 2022 01:19:34 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c635236ace6c57e8af5a6a467722bb1484d5ae5aaf133d60a5475aef5f4d2c4`  
		Last Modified: Tue, 19 Apr 2022 01:19:32 GMT  
		Size: 72.2 KB (72156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9131ef298cbc9163210fbeb93d70aed6922673cebc88b8563ea8ea489357b1c`  
		Last Modified: Tue, 19 Apr 2022 01:19:32 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ed6c834b69ab81bc5dcc57cf62299abe031d36fb332b26b0e30ec3ae7055dc`  
		Last Modified: Tue, 19 Apr 2022 01:19:32 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b22b6c5d0108c193285b2f5dfaeccfe3dbe70b088e5b123bd808e8e3e16493b`  
		Last Modified: Tue, 19 Apr 2022 01:19:43 GMT  
		Size: 101.1 MB (101101137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0f4233f7c135f7a19e6224648557f99b55c6fbcf96b3563b8cda9ab2496fad`  
		Last Modified: Tue, 19 Apr 2022 01:19:32 GMT  
		Size: 58.5 KB (58476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
