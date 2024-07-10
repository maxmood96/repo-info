## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:c1bf05daa01551597c2e19b5f6603f5980cd59201c86fca6818026169ba15d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:37b0dc79c0433d1bdcfdb90eb4d7ba37a99d2c9d46e3a514f86f460321f64d64
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198632638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecedfcefaf28d5636d289238f139f7371153462ef8ae7d33a1e167ebaa81df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 16:46:39 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 10 Jul 2024 16:46:39 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Jul 2024 16:46:40 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 16:46:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 16:46:48 GMT
USER ContainerUser
# Wed, 10 Jul 2024 16:50:51 GMT
COPY dir:b092036da9619d86aad01e40fe92454a038bf12563d3a63208d5f3f51004688a in C:\openjdk-11 
# Wed, 10 Jul 2024 16:51:00 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c254e529e474f59a4578fb2028d068f7b14b05ac32bb741b48bddd3c305f91`  
		Last Modified: Wed, 10 Jul 2024 17:30:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03428648c72b9188308e33592b4f418c573a42c0dd50dfceccedf848fb9cb597`  
		Last Modified: Wed, 10 Jul 2024 17:30:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fe0deee1dde51a87e53a2556f4de0d0653e1e3fb5dabfbe93f5a9e68729dec`  
		Last Modified: Wed, 10 Jul 2024 17:30:24 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc49ab9383cb6875d5fd12ff6e4009a9b34a7ad2037963f0aed12ac4a2127dc`  
		Last Modified: Wed, 10 Jul 2024 17:30:22 GMT  
		Size: 68.9 KB (68922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccd083b75e153d6a232a41157a52842d30b52f61057ee5fe680248fc19eef26`  
		Last Modified: Wed, 10 Jul 2024 17:30:22 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b11ca36be9ee87f7a5123b8be02ed80488c80265f4484022e0a896f2598343`  
		Last Modified: Wed, 10 Jul 2024 17:31:26 GMT  
		Size: 43.4 MB (43384426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59fc55328e7c4be2420940aa3ec30f340c6e69fab2999a3ed33ae93a5408991`  
		Last Modified: Wed, 10 Jul 2024 17:31:20 GMT  
		Size: 92.1 KB (92118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
