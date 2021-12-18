## `eclipse-temurin:16-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:21b4dffb772ed40cba550b7617a8a582c8de36637a55b6e61bf7da8edf561029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `eclipse-temurin:16-jdk-nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull eclipse-temurin@sha256:1d486cec90e1d8c6c0a21b2cdd6a316c50495c8c18d5b89d155c37cb1a3eaed9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305395152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e617e7960e39654cee3df28421d33003649732d5eb6733ad1b6ca52ec16c03`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 05:18:44 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 05:49:21 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Sat, 18 Dec 2021 05:49:22 GMT
ENV JAVA_HOME=C:\openjdk-16
# Sat, 18 Dec 2021 05:49:23 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 05:49:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 18 Dec 2021 05:49:35 GMT
USER ContainerUser
# Sat, 18 Dec 2021 05:49:52 GMT
COPY dir:9a7ef5975d9ba9576c4744dc049616bbcb218f14c3c0bd967851cd46479d6134 in C:\openjdk-16 
# Sat, 18 Dec 2021 05:50:06 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 18 Dec 2021 05:50:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4c557aac927613dd487d7c04b01a8eeb8ad174693f61b14c8f4285f1db6afdd2`  
		Last Modified: Sat, 18 Dec 2021 06:13:05 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8eb691c8553507f92ad782af807ccdb0e69e4e8c8deee9db1379b95c9a04d1`  
		Last Modified: Sat, 18 Dec 2021 06:31:27 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9f5c1711bbd72d9dfb4efc3dfeca7f12887abd470dd03d469247f2afa42490`  
		Last Modified: Sat, 18 Dec 2021 06:31:26 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945bc840bdc185c560ba331b00bd6a32e5a61ae10eda3b072e62b1e0df9f010e`  
		Last Modified: Sat, 18 Dec 2021 06:31:26 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df02ca351ac3340193d0c31d20e2a4f6115416f20274f214c607aeba69105de`  
		Last Modified: Sat, 18 Dec 2021 06:31:24 GMT  
		Size: 75.9 KB (75941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850d68f7297d2cab439762d7a347f5153f49ddb13c3edd1e67b04147d38b7bb1`  
		Last Modified: Sat, 18 Dec 2021 06:31:24 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad9b4940e178f8403678bfbf206581d1fa66ff0baede92567c3bc79155fa75c`  
		Last Modified: Sat, 18 Dec 2021 06:31:46 GMT  
		Size: 198.7 MB (198742442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ff8668825ad6c15ff4ef2a1e172bccdd4e4afe2a24739eba3bfc20ff71b2dd`  
		Last Modified: Sat, 18 Dec 2021 06:31:28 GMT  
		Size: 3.7 MB (3665840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c914e52a30ae16d4011ec29fb91ae14984466bfb2bc7bfc18a2e271cc258cb7d`  
		Last Modified: Sat, 18 Dec 2021 06:31:24 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
