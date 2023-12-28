## `openjdk:22-ea-nanoserver`

```console
$ docker pull openjdk@sha256:a50e0f68444a5ae88eade55e3e2b42d8eaa84491a31766fa3f77d26175897168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `openjdk:22-ea-nanoserver` - windows version 10.0.17763.5206; amd64

```console
$ docker pull openjdk@sha256:fb35aecd984eb10e62c52d53169c1f14fc6e9488ce88fa4a06866009766918b4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305789101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7385ebbbe83d2d3cf7c09165f1470aaf3d7cb51f98a5e3f2d2b08d82bd756bcc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Dec 2023 10:54:04 GMT
RUN Apply image 10.0.17763.5206
# Thu, 28 Dec 2023 02:49:29 GMT
SHELL [cmd /s /c]
# Thu, 28 Dec 2023 02:49:30 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 28 Dec 2023 02:49:31 GMT
USER ContainerAdministrator
# Thu, 28 Dec 2023 02:49:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 28 Dec 2023 02:49:36 GMT
USER ContainerUser
# Thu, 28 Dec 2023 02:49:36 GMT
ENV JAVA_VERSION=22-ea+29
# Thu, 28 Dec 2023 02:49:44 GMT
COPY dir:1f5a0a28361c951316500437ccd447f8727abb0bfbe1de04e97301133c2bb5b2 in C:\openjdk-22 
# Thu, 28 Dec 2023 02:49:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 28 Dec 2023 02:49:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:424f13a93a185a5defe848e7d270655e05233555f51328c0af24b9e70677d037`  
		Last Modified: Tue, 12 Dec 2023 20:02:40 GMT  
		Size: 104.5 MB (104510104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab8af531f3417b0cfe676ad8e4d167c67138b0662919c910e0ebaa205aa2808`  
		Last Modified: Thu, 28 Dec 2023 02:49:57 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93f697fabb53120973d2b510ef9d2f15e7dea406bf5e09cab54b728703b7efa`  
		Last Modified: Thu, 28 Dec 2023 02:49:56 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102f7a8b15e6afbea6d74b6c61727e0aa760a8ba1fdd3153641b78b1ec641764`  
		Last Modified: Thu, 28 Dec 2023 02:49:56 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126c5943d7e5e2435a86a8f936d5383fc3cce3ec347d961b9eff9c08bf86117f`  
		Last Modified: Thu, 28 Dec 2023 02:49:56 GMT  
		Size: 69.0 KB (68991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891e0825cf5b6b0f6f42d98e9053a02e4dc1eb05a104c2a5d16f8fd872426293`  
		Last Modified: Thu, 28 Dec 2023 02:49:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a819aec82131da5327de32f13cb707a3323e38d6fcbc87d569fded8a84ccd54f`  
		Last Modified: Thu, 28 Dec 2023 02:49:54 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfb8fc0d1fb2a6007a4d3ca6dc48d3dc64e1c7186fe0183f6906ce5dceab30b`  
		Last Modified: Thu, 28 Dec 2023 02:50:05 GMT  
		Size: 197.3 MB (197336922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e81a6116c59d8a68c393727a6b29087ae7ed6c6ed3c407bf9415d9ceb0e7f1`  
		Last Modified: Thu, 28 Dec 2023 02:49:55 GMT  
		Size: 3.9 MB (3866863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195cbe2044e74640946b24aa232a66bbbb2e659716c13a1896658ddb401f6148`  
		Last Modified: Thu, 28 Dec 2023 02:49:54 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
