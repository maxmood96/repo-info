## `eclipse-temurin:8u312-b07-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:25a3048f5b4a5dad553bbe4f6cf805ecc596fbbeecb34948006b3901e9b73573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.288; amd64

### `eclipse-temurin:8u312-b07-jre-nanoserver-ltsc2022` - windows version 10.0.20348.288; amd64

```console
$ docker pull eclipse-temurin@sha256:a3e771e8b4e02b4532b86cdd3800e7fbc86bd570ca9581b25b54eb1d4531d5ea
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156185883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022b375afcbc449dd6a8cebcc5e4a59c5ea71f2ccb5ad1cf3a68b724da4a5534`
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
# Fri, 05 Nov 2021 19:44:02 GMT
COPY dir:f43ebde5893522b38a147191e5e447aa435ef67c7d947aeb3e536f25bc61cdb3 in C:\openjdk-8 
# Fri, 05 Nov 2021 19:44:14 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:c44ad19fb5a27fafeaaa77e7d4f10a7d11183eaf730832028390cb96a4413f89`  
		Last Modified: Fri, 05 Nov 2021 20:39:45 GMT  
		Size: 39.1 MB (39087853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfae76da586894d284cc5d965833fc106e98e574ba5b86263e5bed3aa02cfe9f`  
		Last Modified: Fri, 05 Nov 2021 20:39:39 GMT  
		Size: 58.4 KB (58375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
