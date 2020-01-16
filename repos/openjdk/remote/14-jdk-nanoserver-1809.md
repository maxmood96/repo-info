## `openjdk:14-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:8cd774d32beb7ff9f0d85ffe669c73fce0605da56f008c7db7819f954c724bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:14-jdk-nanoserver-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:d9fe38d765a6d8671aad7a75764abe47c84e4cf8e14261954d62f3ffc8f3fb98
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298403376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a1a129754bb0038a9e66e22eab8780d193bfa524243378f24317e9189e9582`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Tue, 14 Jan 2020 23:56:11 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2020 00:05:42 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 15 Jan 2020 00:05:43 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2020 00:05:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 15 Jan 2020 00:05:57 GMT
USER ContainerUser
# Wed, 15 Jan 2020 23:54:17 GMT
ENV JAVA_VERSION=14-ea+31
# Wed, 15 Jan 2020 23:55:26 GMT
COPY dir:2ac7fd25e7442d7bd2a532a31f593383cd5f56d4c4c47219a9bfcfface66e3f3 in C:\openjdk-14 
# Wed, 15 Jan 2020 23:55:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 15 Jan 2020 23:55:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:764e25aa4e95684bd69a4d130dc1c729bfaef95293d9c76c4d2a12ced9e3a9ac`  
		Last Modified: Wed, 15 Jan 2020 01:51:06 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f3a5df9926db070e4016e42e49a7d9ce0131f528e644ae4388774831b6b46e`  
		Last Modified: Wed, 15 Jan 2020 01:58:21 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c21d67a14cad5558f706984eed7f97aaa2665e4b4cf1a7a1d21888c5e2c02a2`  
		Last Modified: Wed, 15 Jan 2020 01:58:20 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ffd38236cfc5913ab84e035b74a0bddf197bbfffdd8e9e8b151cc30bbf8adb`  
		Last Modified: Wed, 15 Jan 2020 01:58:20 GMT  
		Size: 66.5 KB (66486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8510d836b27dbac14cee7131c4209ebf2081c2ba957f75e05cbeff605e5320`  
		Last Modified: Wed, 15 Jan 2020 01:58:18 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb78c4310dba86fc152a22079f6072a053b1b0c0f751a1edeba490c5f8ebddf`  
		Last Modified: Thu, 16 Jan 2020 00:21:50 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187204fe685a7a223b13259fb1ed0cefd2d7b4fcf3df0338ac2f4941790b7d37`  
		Last Modified: Thu, 16 Jan 2020 00:22:12 GMT  
		Size: 193.8 MB (193830284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b9cfb8ac17fd48b9eb25a2e3d5e50ec2c696e24d87ff8f8aab759e0c4a8baf`  
		Last Modified: Thu, 16 Jan 2020 00:21:53 GMT  
		Size: 3.4 MB (3446679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c97ce107ac558e8737d7c73a0cf6eae4c405239ace82dfbf8318373f93c25`  
		Last Modified: Thu, 16 Jan 2020 00:21:50 GMT  
		Size: 925.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
