## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c0dd34d7bcd19363b875512c0d6c73de0e431c3685a153a0c7eef1a0a735e105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull eclipse-temurin@sha256:700aae79831cf67a8ca2924444fcf9e54365446aeadea5e848c63149eb604ffb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161575055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9294708b667a034e242e63c675e9bebad2d7a02de81d780ddeb46f075cef966a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Jan 2023 23:36:49 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 02:19:48 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 02:19:48 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Thu, 12 Jan 2023 02:19:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 12 Jan 2023 02:19:50 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 02:20:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 12 Jan 2023 02:20:14 GMT
USER ContainerUser
# Thu, 12 Jan 2023 02:21:09 GMT
COPY dir:4e862dd3e9e3173048336ba652726d009cc7bbbadd67bc711cdb421cf611c5ab in C:\openjdk-8 
# Thu, 12 Jan 2023 02:21:28 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:83e9437e818022c1c28f0e07002dd46995c8614e62b9366138fa23b94f43d9ad`  
		Last Modified: Thu, 12 Jan 2023 02:51:06 GMT  
		Size: 122.1 MB (122099566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbebbf572ebe7984b715b8dfe99bc1273403a831c0079b95afa12162b7266f16`  
		Last Modified: Thu, 12 Jan 2023 02:50:38 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac7d468bdb6a099795ee184e23d7c26764a8e451ec0477faec012ae08ff63b5`  
		Last Modified: Thu, 12 Jan 2023 02:50:38 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdcadd904c8aa3749640e7e5de4ca50b3f0a2afafbf20eecfa5c32ed84ac24b`  
		Last Modified: Thu, 12 Jan 2023 02:50:38 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78325accf82cc30e1a1cf2683c75b74be6551a4ddfa229082958effb18b94d72`  
		Last Modified: Thu, 12 Jan 2023 02:50:36 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fddfac47d5b4f83760df7fc4954f4419a399914dbe8d8455c83e3ee7b76e86`  
		Last Modified: Thu, 12 Jan 2023 02:50:36 GMT  
		Size: 87.8 KB (87828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483c6db44e09d3f3f97e05de8cbf54ded06c9f8d9cdddc65b7f941587e1f5f73`  
		Last Modified: Thu, 12 Jan 2023 02:50:36 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b39ce57c0577970f740f33a4be28df220fb048dcba921dbaac23fdfdfe9fa9d`  
		Last Modified: Thu, 12 Jan 2023 02:51:23 GMT  
		Size: 39.3 MB (39323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b719332cf750f59ccb18b7d63b2cc8b31ca1167457431a2841b874127a65fb`  
		Last Modified: Thu, 12 Jan 2023 02:51:16 GMT  
		Size: 58.7 KB (58689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
