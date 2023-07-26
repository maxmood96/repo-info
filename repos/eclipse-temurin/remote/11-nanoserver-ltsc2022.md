## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:f20e1d0fa4c78a7a61254e47aa27d39a582f6611a72b19b0a79aa05126fb6914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:94b81aa67c4a1edea1d911bfeaf3d577fb0aeb19dd2ae1310c998080b36c686a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313311638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec359935d859ac9e0154e159115755c65f3836d74aeb99a41b770635f7a9373`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 21:00:40 GMT
RUN Apply image 10.0.20348.1850
# Thu, 13 Jul 2023 22:10:51 GMT
SHELL [cmd /s /c]
# Wed, 26 Jul 2023 00:27:24 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:27:25 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 26 Jul 2023 00:27:25 GMT
USER ContainerAdministrator
# Wed, 26 Jul 2023 00:27:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 26 Jul 2023 00:27:36 GMT
USER ContainerUser
# Wed, 26 Jul 2023 00:27:50 GMT
COPY dir:0494f0c3004dc0f4e40e3f6c0c6e0f2ac35120ffc9906421c49b5c62e99eee70 in C:\openjdk-11 
# Wed, 26 Jul 2023 00:28:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:28:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc0a26bd90fcc4d863317c36d7ffec77a0a82a905697204d4dcbc76ec13b3920`  
		Last Modified: Tue, 11 Jul 2023 20:10:45 GMT  
		Size: 120.1 MB (120056465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb11750b624a775aa3c21a13406dfc54458855b8684e21efba5bbb9b27ee0b12`  
		Last Modified: Thu, 13 Jul 2023 22:28:35 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6fc7da52cd85c46d7cc9f4b0fe25d75d7e3cfcaa2dfc65ebac000529276d57`  
		Last Modified: Wed, 26 Jul 2023 00:34:25 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835a4cdfb9b1958fb13255c78147171f9d8747a6fa5a2719e6bfc9da55fd9f88`  
		Last Modified: Wed, 26 Jul 2023 00:34:25 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46453ada3c9c1d0d1c66cf1fc4b47ec80b2e70a8efc7bc57d3032202abebf733`  
		Last Modified: Wed, 26 Jul 2023 00:34:25 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075d5243707d8e6924ce011650fd2ae3e47c22405846bcbf95e4307ed0f9da5e`  
		Last Modified: Wed, 26 Jul 2023 00:34:24 GMT  
		Size: 80.2 KB (80184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18907ca6b61aec2fab8b9c92eba73443a66ae1c03a167e26d6be34a7ba63020`  
		Last Modified: Wed, 26 Jul 2023 00:34:23 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baccff07c79e264703937b14194e48bab60b8cca253468921fd0d65aad34b1c2`  
		Last Modified: Wed, 26 Jul 2023 00:34:43 GMT  
		Size: 193.1 MB (193107061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbcd3d0b8d3f3c4914a5bee882ce0b2f241324d5d3ee4ca699fa3b79ec2e23c2`  
		Last Modified: Wed, 26 Jul 2023 00:34:23 GMT  
		Size: 61.0 KB (61009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3611dd2d2e0c0ec88f5265990bb2e6d608743e6a81ccf7635148f5a85397c748`  
		Last Modified: Wed, 26 Jul 2023 00:34:23 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
