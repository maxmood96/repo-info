## `eclipse-temurin:8u345-b01-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c78e2972bd107a4ab17100b1dd3a4ddec1abfbfd14676477f05a339c4bef3576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:8u345-b01-jre-nanoserver` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:0a77511c89980aae93bf77851eee267fd1ef78a96f5fe42356e8b916bde36891
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157674909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb338ddb5eb1fa05b63bfffc349a13887ac9a2e7c18dabe76652b2f345fa352c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 15:54:21 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 15:54:21 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 12 Oct 2022 15:54:22 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Oct 2022 15:54:23 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 15:54:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Oct 2022 15:54:37 GMT
USER ContainerUser
# Wed, 12 Oct 2022 15:55:17 GMT
COPY dir:8b6137b055df5a3c6f914a172c41a8287046696fe7ccc91d96608246e3752adc in C:\openjdk-8 
# Wed, 12 Oct 2022 15:55:29 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:38fa349577729651ac1fc3ec785f908719a8100da5f5ba9bd3f549411061f583`  
		Size: 118.2 MB (118202895 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0ed0041e3584df1952980c3f73fd2b6e154328c7a0165f37dbe92ef94ae8a95`  
		Last Modified: Wed, 12 Oct 2022 16:12:53 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812a04e8585e8b3fa1625525f7078c3fe8bdc3552beb86abe3186aeaf9332b2d`  
		Last Modified: Wed, 12 Oct 2022 16:12:53 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ef3610b04a50a6280701b19afc7e8b37b0d80c7e83845179c546c7890b1914`  
		Last Modified: Wed, 12 Oct 2022 16:12:53 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56128496f65019ddc28a9cde56ac2a0be3562bafdd0b336e9ee10ff364876210`  
		Last Modified: Wed, 12 Oct 2022 16:12:50 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfc3a606e27a41483ff4916dccc96b24730ef6ad9dbc0a2deb76341e07a3745`  
		Last Modified: Wed, 12 Oct 2022 16:12:50 GMT  
		Size: 85.4 KB (85425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ad17f557c1d2566ec24fc1e66666d4f818ee093ff0b5275dd7b6a2256a3b94`  
		Last Modified: Wed, 12 Oct 2022 16:12:50 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0961dba2fd976cc384d5b490fd24d7aebb35760649a5d2dfc7d2f1193951ef`  
		Last Modified: Wed, 12 Oct 2022 16:13:21 GMT  
		Size: 39.3 MB (39318725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881bad79f01f9baf6b695ff59ce571acfcb71170d97774e527930b034fe7299f`  
		Last Modified: Wed, 12 Oct 2022 16:13:15 GMT  
		Size: 62.1 KB (62149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u345-b01-jre-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:9218624cf08ea1cfaa8a65c0b3f8be3aadf365b966e8eac0d5a495505c41bd8b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142849737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741a1946e9abe62ea106d3619ef9b5f21bc741ef9ab4b9fc7a06795eb499b2e5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Wed, 12 Oct 2022 15:20:49 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 15:20:50 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 12 Oct 2022 15:20:50 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Oct 2022 15:20:51 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 15:21:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Oct 2022 15:21:05 GMT
USER ContainerUser
# Wed, 12 Oct 2022 15:26:00 GMT
COPY dir:8b6137b055df5a3c6f914a172c41a8287046696fe7ccc91d96608246e3752adc in C:\openjdk-8 
# Wed, 12 Oct 2022 15:26:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a6a667d76c19fca171390d60fb90c40e16c777050e943a7fe17ad7686841f0f`  
		Last Modified: Wed, 12 Oct 2022 16:02:59 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b821bdf95869001729985837164936fdea83eda60a0c33659cead92995aea0cb`  
		Last Modified: Wed, 12 Oct 2022 16:02:59 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409e22156b1f46adc58d43ec69be4b38ebe223e9eb94663cfc164dc78e7379e0`  
		Last Modified: Wed, 12 Oct 2022 16:02:59 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02003dd7b958504849592641e375564443510516dc147dc2bbbd683635846ad`  
		Last Modified: Wed, 12 Oct 2022 16:02:57 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2ec4bc651f60d02bda9aabef3a9c77736de5df7d69640347ebcc51bd3d206`  
		Last Modified: Wed, 12 Oct 2022 16:02:57 GMT  
		Size: 70.4 KB (70443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc148a3d04e196ece6cb83bb3929dd48816ae38f2cf5fe239f06c8fcb54f9495`  
		Last Modified: Wed, 12 Oct 2022 16:02:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9a7d5633e2911af4d537eef316288a017cf89b6e955104eb24058c799e7adc`  
		Last Modified: Wed, 12 Oct 2022 16:04:03 GMT  
		Size: 39.3 MB (39314207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68797f534718d46a00aa7d597efe59bd3bc5174d077429b11db5ea266371cb34`  
		Last Modified: Wed, 12 Oct 2022 16:03:58 GMT  
		Size: 82.1 KB (82089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
