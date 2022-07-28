## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:c9e2b8d448865dc27228a4fd8677f3f6fa06c9b596ac49f3374622eb2a2b0e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull eclipse-temurin@sha256:c3ab52dabd32b73cb4c1996ba170b8371a22cc355bf8eb81ae205a319c322dd2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295685152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eba534d1c2308ec60031a48514a45b2d71ca388a9734375d07e56932ae6a665`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Thu, 28 Jul 2022 16:21:12 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:21:13 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 28 Jul 2022 16:21:14 GMT
USER ContainerAdministrator
# Thu, 28 Jul 2022 16:21:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 28 Jul 2022 16:21:30 GMT
USER ContainerUser
# Thu, 28 Jul 2022 16:21:45 GMT
COPY dir:311b50e59d3b0be0ca838f3cd712deaf9388198aeb821aea34d4de0537bd9b6e in C:\openjdk-11 
# Thu, 28 Jul 2022 16:22:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:22:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea12bb691aaa5d39e320d6c853d1f72c4f8a5cf6ea617ae2993a322713c92bcc`  
		Last Modified: Thu, 28 Jul 2022 16:44:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb07b488c8049fc65ecfb4ece07bd17ca87edc4bc3a924090d12c38a915a89c`  
		Last Modified: Thu, 28 Jul 2022 16:44:40 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4af14d5e4431703d40fe5c49f8ddd4cf832f851de381cfc75cd5e101f9d07f0`  
		Last Modified: Thu, 28 Jul 2022 16:44:40 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c60b48cbcf85422570b793d7032b6f380d04f09aea72ecaf4b378309ccff98e`  
		Last Modified: Thu, 28 Jul 2022 16:44:38 GMT  
		Size: 70.6 KB (70584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6b078b4a6303e9ef5314be0c4dac84047bc0b7226e9591025e14f1e56777b`  
		Last Modified: Thu, 28 Jul 2022 16:44:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74f82cbe26f37c6e0fd1db0bd405ed1cce701a5ba747b252cb8d61a085b6790`  
		Last Modified: Thu, 28 Jul 2022 16:44:57 GMT  
		Size: 192.4 MB (192370323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de33372ff17d6aced764fbc88654b2de0ab2ab91be9181d36c13a871f99fff81`  
		Last Modified: Thu, 28 Jul 2022 16:44:37 GMT  
		Size: 82.3 KB (82340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb658fa172b4ec8498e211f308ddbef34ce0767d0bbbeffa6d52dfeb3efaab0`  
		Last Modified: Thu, 28 Jul 2022 16:44:37 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
