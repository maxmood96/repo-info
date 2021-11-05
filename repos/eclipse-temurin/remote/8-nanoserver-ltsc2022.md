## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:2ba8df3a5773c63011bf6bd50a70a31fe9cbf6e5b7fb6ba9db595d01ed782624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.288; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.288; amd64

```console
$ docker pull eclipse-temurin@sha256:0254fb746d33d931e3df0dc282c3a5fa74dd4c4564fadbfc48fd261f68925e7f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217293441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13da8ffe4108cc75e2e998d3b3eb7fe9f6e4eeb37b8307bf7e3b925b43d0d061`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 11:15:04 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Oct 2021 19:02:30 GMT
SHELL [cmd /s /c]
# Fri, 05 Nov 2021 19:43:06 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 05 Nov 2021 19:43:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 05 Nov 2021 19:43:07 GMT
USER ContainerAdministrator
# Fri, 05 Nov 2021 19:43:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 05 Nov 2021 19:43:22 GMT
USER ContainerUser
# Fri, 05 Nov 2021 19:43:32 GMT
COPY dir:7d20e7860b874019800a6393f3930849559cf997f64b86d2d0263d858293fa37 in C:\openjdk-8 
# Fri, 05 Nov 2021 19:43:46 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:91284e7e8fd4bd7ebcfa98544a3e4f59639f38281225c81c34b6fe22e0dba4e5`  
		Size: 116.9 MB (116939483 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ba797e8f93823c3d71c52fcae413f3a33ca28ff2711c09ba5141432948f8298`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9dec6b507607ca08e638c7d3ae3128972c49650144c514f4c38fc57ceb5c43`  
		Last Modified: Fri, 05 Nov 2021 20:39:18 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9a6e263cf49da630f6760ba1b585fef5f0428dd256021064f116c34a3d2b98`  
		Last Modified: Fri, 05 Nov 2021 20:39:17 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee96e2b9d26ffc56e72b87fb9a7157aef8e02be14bc87c86f5eec89c492dc13`  
		Last Modified: Fri, 05 Nov 2021 20:39:15 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a309d0ae1eba4bee66a057c942a2f0bc3ecf5ce3637bb386e7302db6911bc8f3`  
		Last Modified: Fri, 05 Nov 2021 20:39:15 GMT  
		Size: 94.4 KB (94354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb7d50903a50966a72f48c7e65fa918cc57be153a73d494e86add07b2e55b9`  
		Last Modified: Fri, 05 Nov 2021 20:39:15 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7781661bd241457bca31a37c54819b089170552672f784676cccd3d49f1784`  
		Last Modified: Fri, 05 Nov 2021 20:39:27 GMT  
		Size: 100.2 MB (100187455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b984f6a8128dc7f416c473137ec4c4e859a43329261f55f319abdce761f637`  
		Last Modified: Fri, 05 Nov 2021 20:39:15 GMT  
		Size: 66.3 KB (66331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
