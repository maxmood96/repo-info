## `openjdk:26-ea-32-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:b90435191ff1de71f43091b877fc654bd08c82502bc00785b4a00ba6d7b5f1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-32-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:d41a4e9c53012ba1f629148f501fbcc8475bc74ed9fa9ce515ef3a122e28a3f8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350788778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3226dcb1033457f04f6930de2e3e1e1d4a840877d2b1d4f2a67d5634d16cd2e6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Mon, 26 Jan 2026 23:12:36 GMT
SHELL [cmd /s /c]
# Mon, 26 Jan 2026 23:12:39 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 26 Jan 2026 23:12:40 GMT
USER ContainerAdministrator
# Mon, 26 Jan 2026 23:12:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 26 Jan 2026 23:12:54 GMT
USER ContainerUser
# Mon, 26 Jan 2026 23:12:55 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 23:14:08 GMT
COPY dir:1413f25fe2f5e950fbcb1d8e8eb2b3797092a9f87fa5ca5a59c32e02bcbf5aa0 in C:\openjdk-26 
# Mon, 26 Jan 2026 23:14:15 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 26 Jan 2026 23:14:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e51f20a630010d929dc6108e426f6d138555f634eb15711b6e888053888c8f`  
		Last Modified: Mon, 26 Jan 2026 23:14:23 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dabdd7f6091b020304e60a143feba4078aeb0d2f0f6593cf2a6fe20d93ae847`  
		Last Modified: Mon, 26 Jan 2026 23:14:23 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186cf8d9c9fffc47ad73bad0507de72a5a0d79669c233c6840d62cbe33ff1c6c`  
		Last Modified: Mon, 26 Jan 2026 23:14:22 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0eb7cf4adad6ba80ee6f5fc06d7baed3227262cbcf29fa659a1d182c0fc45`  
		Last Modified: Mon, 26 Jan 2026 23:14:22 GMT  
		Size: 75.1 KB (75113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fb2cdc257cce10bc68d9da6b2cd64adbdfe6d713a96659382f51db39889a85`  
		Last Modified: Mon, 26 Jan 2026 23:14:21 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510a1f982da878ab59836274536e431e01b41053e371e83a08eb3a4558c757f0`  
		Last Modified: Mon, 26 Jan 2026 23:14:21 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394f2ad9c38010e72abc73292805c8635dd5fb617d53d2d3894cc8596d3e1620`  
		Last Modified: Mon, 26 Jan 2026 23:14:36 GMT  
		Size: 223.9 MB (223878435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dba2a242631046553bd0e3179a34563a167eb832742911d9f272598c382819`  
		Last Modified: Mon, 26 Jan 2026 23:14:21 GMT  
		Size: 132.0 KB (131954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18bdca7291a08e420fb51ad0f90cd29651ce8f0a4ee83d24b2dc9b8b7b112a2`  
		Last Modified: Mon, 26 Jan 2026 23:14:20 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
