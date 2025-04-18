## `eclipse-temurin:24_36-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b693a8ca35ed026aaef1cf1ae3d6a2bb0809636167b36c48e0b4c4587c904ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:24_36-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:b36595df4e61da3c715a3f902e6d0500b70a38b89b9bb3e6de9bb4b3500484f1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180428152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e57da52254538312d98d52f649507d3b5301b386eb118688bbc024ed92508ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:16:09 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:16:09 GMT
ENV JAVA_VERSION=jdk-24+36
# Fri, 18 Apr 2025 04:16:10 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 18 Apr 2025 04:16:11 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:16:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:16:14 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:16:19 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Fri, 18 Apr 2025 04:16:24 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c022bb6e1e619d8b2032cf6b93ab9a319c3cb44f21dd42561d29c0df725f73`  
		Last Modified: Fri, 18 Apr 2025 04:16:27 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d140dc61c35505c0f00b304c5a81676031bbdad8c8fd56d868eabda73c927b22`  
		Last Modified: Fri, 18 Apr 2025 04:16:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ede6cfd5a06bbf9bff3d1c3c6278559fcfd5ee19026d8d86a2d3bacc1b27c0`  
		Last Modified: Fri, 18 Apr 2025 04:16:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abcafd02fb4d5abd90dbdfc2060e0163b3961cb3ecf0557ab177a695da1166a8`  
		Last Modified: Fri, 18 Apr 2025 04:16:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9b6f598e53eb22aa4e29e607d678c401ff1c7dac256f4873ad492080c75de2`  
		Last Modified: Fri, 18 Apr 2025 04:16:26 GMT  
		Size: 76.8 KB (76787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3723571d74ae436416b8b1c676cff9148e5044f7460b7c2646356e1c9fc89dd`  
		Last Modified: Fri, 18 Apr 2025 04:16:26 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2774dfb378ef2f6a582e97114b3dc434a9bf35f205b59bb3f4b33e2a24454d87`  
		Last Modified: Fri, 18 Apr 2025 04:16:33 GMT  
		Size: 57.7 MB (57700665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75878bae5569e89ec743494bdf1b54cba4143fdc0109b0fec57b181b751b1b1b`  
		Last Modified: Fri, 18 Apr 2025 04:16:26 GMT  
		Size: 106.5 KB (106469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
