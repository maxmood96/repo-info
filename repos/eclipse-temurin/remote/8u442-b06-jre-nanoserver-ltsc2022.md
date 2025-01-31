## `eclipse-temurin:8u442-b06-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:501dacec3140b470153ce4df9230ebb0d8c96b9a976e7358e63534c532bbbb20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:8u442-b06-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:39523b67fb31671fff719147b51823f6c9d5405c637c693491443362b279aac7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161381772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed199c30648b804b08414b37034adea06ac1c3aa2de32a06f8d109afed38560`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Fri, 31 Jan 2025 03:12:21 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 03:12:22 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 03:12:22 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 31 Jan 2025 03:12:23 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 03:12:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 03:12:42 GMT
USER ContainerUser
# Fri, 31 Jan 2025 03:12:45 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Fri, 31 Jan 2025 03:12:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ede267650c4c8a83b809671e8f80bc36b669b460f97b76751a2ebb44ca4807f`  
		Last Modified: Fri, 31 Jan 2025 03:12:52 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e062fbc92032ed8b98f9b45117a4b7ea519a9afe022ed63b7192d859737f4a`  
		Last Modified: Fri, 31 Jan 2025 03:12:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfc8f4b25c3ace13f91d6a010b70f85278735dcc4e22863b1e5c5a7a0290454`  
		Last Modified: Fri, 31 Jan 2025 03:12:52 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8193da053c6ad34a7a57a8d7bb2279ae7838522f966832d00f250aa80c9fa39`  
		Last Modified: Fri, 31 Jan 2025 03:12:51 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d6111b49c7b560574cefe0d6fccf6e4a21e6db2365dda0f764a4d08454d39b`  
		Last Modified: Fri, 31 Jan 2025 03:12:51 GMT  
		Size: 72.9 KB (72893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128bacfa36c823d63b98824e68aa781199b2af72ae1b39c37aae42b783561a71`  
		Last Modified: Fri, 31 Jan 2025 03:12:51 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe599b534ddc55b799e38d38b255a7d7ce9de21ad2704ebfede7c79f65d8842c`  
		Last Modified: Fri, 31 Jan 2025 03:12:55 GMT  
		Size: 40.6 MB (40552211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5c1cb27573addcc9594fec8cabba010241a923d8f6a4b591639d247646ff36`  
		Last Modified: Fri, 31 Jan 2025 03:12:51 GMT  
		Size: 89.9 KB (89925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
